FROM mcr.microsoft.com/dotnet/sdk:7.0.400

# Install CA certificates (important for SSL issues)
RUN apt-get update && \
    apt-get install -y ca-certificates && \
    update-ca-certificates

# Install dotnet-sonarscanner tool globally
RUN dotnet tool install --global dotnet-sonarscanner --version 10.2.0 

# Make global tools available in PATH
ENV PATH="${PATH}:/root/.dotnet/tools"
