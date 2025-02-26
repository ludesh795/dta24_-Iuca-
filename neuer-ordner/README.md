# Schritt 1: Basis-Image für ASP.NET Core Applikationen verwenden
FROM mcr.microsoft.com/dotnet/aspnet:6.0 AS base

# Schritt 2: Arbeitsverzeichnis festlegen
WORKDIR /app

# Schritt 3: Dateien in das Container-Image kopieren
# Hier wird der gesamte Inhalt des aktuellen Verzeichnisses (z.B. Ihr Projektverzeichnis) in das /app Verzeichnis im Container kopiert
COPY . .

# Schritt 4: Den Befehl zum Starten der Applikation definieren
# Hier wird die DLL der Applikation angegeben, die gestartet werden soll
ENTRYPOINT ["dotnet", "ContactManager.dll"]
