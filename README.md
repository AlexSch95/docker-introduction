### Das "Works on my machine"-Problem: Welchen entscheidenden Vorteil bietet dein Docker-Container im Vergleich dazu, wenn du einem Kollegen einfach nur deinen Code-Ordner schicken würdest? 
- Mit Docker hat man immer die exakt gleiche infrastruktur, egal wo man den Container buildet / startet, da im Dockerfile alle gegebenheiten festgelegt sind (z.B. Packageversionen usw)  
---
### Blaupause für die Infrastruktur: Erkläre in deinen eigenen Worten, warum das Dockerfile als "Infrastructure as Code" bezeichnet werden kann. 
- Weil der Bauplan der Infrastruktur für die Anwendung bzw den Container quasi Code ist, Wir sagen Docker alles nötige um den Container so zu bauen, dass unsere Anwendung perfekt läuft sodass keine inkonsistenzen entstehen können
---
### Trennung von Code und Abhängigkeiten: Warum ist es (insbesondere bei Node.js und Python) eine gute Praxis, die Abhängigkeiten (node_modules oder virtuelle Umgebungen) nicht direkt in das Image zu kopieren, sondern sie durch einen RUN-Befehl im Dockerfile installieren zu lassen?
- Im endeffekt gibt es viele variablen die sich auf die Funktionalität auswirken können, wenn wir also einfach die Node-Modules die bei uns installiert sind, direkt mit in den Container packen würden statt beim Starten des Containers die Pakete frisch zu installieren, könnte es passieren dass unter unterschiedlichen Gegebenheiten unsere Anwendung nicht läuft / probleme verursacht
---
### Ports: Was ist der Unterschied zwischen dem Port, den du mit EXPOSE im Dockerfile angibst, und dem Port, den du im docker run -p Befehl verwendest?
- So wie ich das verstehe ist das EXPOSE im Docker-File die einstellung für den Internen Port des Docker Containers, im run befehl wird dann festgelegt unter welchem port man mit dem Docker COntainer kommuniziert bzw auf die Inhalte zugreift
---
![screenshot](https://i.imgur.com/zFana6v.png)
