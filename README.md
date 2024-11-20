# ict-m324 / Task 1 NPM

# Building and Package Management with NodeJS (JavaScript)

## Voraussetzungen

- Überprüfen Sie in einem Terminal mit `node -v` und `npm -v`, ob NPM korrekt installiert ist.
- Wenn nein, folgen Sie den Anweisungen hier (https://docs.npmjs.com/downloading-and-installing-node-js-and-npm). Überprüfen Sie mit obigen Befehlen, ob die Installation erfolgreich war.

## Build-Automatisierung mit Node.js

1. **Projekt Setup**:

   - Erstellen Sie ein neues Verzeichnis für Ihr Projekt und initialisieren Sie ein neues Node.js-Projekt.
     ```bash
     mkdir my-project
     cd my-project
     npm init -y
     ```
   - Erstellen Sie eine `index.js` Datei:
     ```javascript
     // index.js
     console.log("Hello, World!");
     ```

2. **Script zum Starten des JS**:

   - Bearbeiten Sie die `package.json` Datei, um ein Startskript hinzuzufügen:
     ```json
     {
       "name": "my-project",
       "version": "1.0.0",
       "scripts": {
         "start": "node index.js"
       },
       "dependencies": {}
     }
     ```
   - Führen Sie das Skript aus:
     ```bash
     npm run start
     ```
   - Das sollte die Nachricht "Hello, World!" in der Konsole ausgeben.

## Software Pakete installieren

- Installieren Sie ein Paket, das die Konsole einfärbt: https://www.npmjs.com/package/chalk:

```bash
npm install chalk
```

- Verwenden Sie `chalk`, um die Ausgabe in der Konsole grün einzufärben. Tipp: Fügen Sie folgende Zeile im package.json hinzu und verwenden Sie import in der JS Datei:

```
  "type": "module",
```

## Software Pakete updaten

- Installieren Sie [npm-check-updates](https://www.npmjs.com/package/npm-check-updates)
- Da Sie das Paket gerade installiert haben, gibt es noch keine Updates. Ändern Sie die Version ihrer NPM Pakete, zB.
  "chalk": "^5.3.0" => "chalk": "^5.2.0"
- Führen Sie npm-check-updates aus und achten Sie auf die Ausgabe.
- Führen Sie das Update aus.

## Konflikte lösen

- Führen Sie `npm install eslint@3.12.1` aus.
- Anschliessend `npm install babel-eslint@10.1.0`
- Es tritt ein Problem auf. Achten Sie auf die Fehlerausgabe.
- Welche Version von welchem Paket ist die Mindestanforderung?
- Für Security ist es wichtig, dass Software stets geupdated wird. Nutzen Sie npm-check-updates, um alle Pakete zu updaten.

## NPM Registry durchsuchen

- Installieren Sie ein beliebiges weiteres NPM Paket. Suchen Sie ein Paket bei https://www.npmjs.com/ aus. Achten Sie darauf, welche Dateien im Ordner node_modules abgelegt werden.
