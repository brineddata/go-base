FROM postgres:17

COPY init.sql /docker-entrypoint-initdb.d/

# Add a health check
HEALTHCHECK --interval=5s --timeout=5s --retries=5 CMD pg_isready -U postgres -d myapp