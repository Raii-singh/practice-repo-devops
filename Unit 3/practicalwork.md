version: '3.8'

services:
  # 1. Database Tier
  db:
    image: postgres:15-alpine
    container_name: postgres_db
    restart: always
    environment:
      POSTGRES_DB: ${POSTGRES_DB}
      POSTGRES_USER: ${POSTGRES_USER}
      POSTGRES_PASSWORD: ${POSTGRES_PASSWORD}
    ports:
      - "5432:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data # Fulfills: Data Persistence
    # A healthcheck ensures the DB is fully ready to accept connections
    healthcheck:
      test: ["CMD-SHELL", "pg_isready -U ${POSTGRES_USER} -d ${POSTGRES_DB}"]
      interval: 10s
      timeout: 5s
      retries: 5

  # 2. Backend Tier
  backend:
    build: 
      context: ./backend
    container_name: springboot_api
    restart: always
    ports:
      - "8080:8080"
    environment:
      SPRING_DATASOURCE_URL: ${SPRING_DATASOURCE_URL}
      SPRING_DATASOURCE_USERNAME: ${POSTGRES_USER}
      SPRING_DATASOURCE_PASSWORD: ${POSTGRES_PASSWORD}
    depends_on: # Fulfills: Dependency Order
      db:
        condition: service_healthy # Waits for the DB healthcheck to pass

  # 3. Frontend Tier
  frontend:
    build:
      context: ./frontend
    container_name: react_frontend
    restart: always
    ports:
      - "3000:3000"
    environment:
      - REACT_APP_API_URL=${REACT_APP_API_URL}
    depends_on:
      backend:
        condition: service_started # Waits for backend container to start

# Fulfills: Data Persistence
volumes:
  pgdata:
    driver: local




    