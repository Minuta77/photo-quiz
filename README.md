Foto‑Quiz — lokale Web‑App

Kurzanleitung (Deutsch)

1) Bilder vorbereiten
- Lege deine Bilder im Ordner, z.B. "C:/Users/DEINNAME/Pictures/QuizBilder" ab.
- Das Projekt erwartet, dass du das PowerShell‑Skript `import_images.ps1` ausführst, welches die ersten 100 Bilder in das lokale Projektverzeichnis `photo-quiz/quiz-images/` kopiert und eine `images.json` mit der Dateiliste erzeugt.

2) Bilder importieren (einmalig)
- Öffne PowerShell und navigiere zu `c:\Users\fixcmo5\photo-quiz`.
- Passe im Skript `import_images.ps1` den Pfad `\$sourceDir` an deinen Bilder‑Ordner an (Standard ist `C:\Users\FIXCMO5\Pictures\QuizBilder`).
- Führe:

  ```powershell
  .\import_images.ps1
  ```

3) App öffnen
- Öffne `index.html` im Browser (am besten per lokalem Webserver, z. B. `python -m http.server 8000` im Ordner `photo-quiz` und dann http://127.0.0.1:8000/ ).
- Die App lädt automatisch bis zu 100 Bilder aus `quiz-images/` und generiert das Quiz.

Wichtig: Browser‑Sicherheit erlaubt nicht immer das Laden lokaler Dateien über `file://`; daher ist ein kleiner lokaler Server empfehlenswert.

Datenschutz & Hinweise
- Reverse‑Geocoding nutzt die OpenStreetMap Nominatim API, um aus GPS‑Koordinaten Ort/Region/Land zu ermitteln. Dieses Anfrage‑Verhalten kann öffentliche Server kontaktieren.
- Wenn ein Bild keine Geodaten hat, wird es übersprungen und im Bereich „Bilder ohne Standort“ gelistet.

Wenn du möchtest, passe ich das Design noch an oder erweitere die lokale Import‑Logik. Viel Spaß beim Testen!
