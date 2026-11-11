# Technischer Aufbau des Eckernkamp-Kompass

Der **Eckernkamp-Kompass** ist ein innovatives KI-gestütztes System, das Projektverantwortlichen dabei hilft, realistische Stakeholder-Interviews und Gruppendiskussionen zu simulieren. Da echte Stakeholder-Befragungen oft zeitaufwendig und teuer sind, greift das System auf eine fundierte Basis aus echten Studien, Berichten und qualitativen Interviews zurück. 

Der technische Aufbau gliedert sich in vier Hauptkomponenten:

---

## 1. Der Suchagent (Automatisierte Literaturrecherche & Prüfung)
https://github.com/Shift-Institut-organization/agentic-research-skills

Der Suchagent fungiert als digitaler, unermüdlicher Rechercheassistent. Er durchsucht automatisiert wissenschaftliche und öffentliche Datenbanken nach relevanten Studien, Berichten und Datensätzen.

* **Recherche:** Der Agent durchquert große Forschungsplattformen (wie OpenAlex, Crossref, Zenodo oder arXiv) sowie das Web, um bis zu Hunderte relevante Quellen zu sammeln.
* **Lizenz- und Datenschutzprüfung (DSGVO):** Jede gefundene Quelle wird von einem weiteren Agenten automatisiert geprüft. Das System stellt sicher, dass urheberrechtliche Nutzungsrechte vorliegen und keine geschützten personenbezogenen Daten (wie unverblindete Zitate) unzulässig verarbeitet werden. Wenn Quellen nicht automatisiert geprüft werden können, werden sie von SHIFT geprüft. Nur freigegebene Dokumente kommen in die nächste Stufe.
* **Anforderungsanalyse:** Weitere Analysekomponenten werten die freigegebenen Inhalte aus und leiten daraus automatisch relevante Stakeholder-Gruppen, Interessenkonflikte sowie grundlegende Nutzer-Personas ab.

---

## 2. RAGFlow (Das intelligente Wissens- und Gedächtniszentrum)
https://github.com/infiniflow/ragflow

**RAGFlow** (eine Open-Source-Software zur wissensbasierten KI-Steuerung) bildet das Herzstück des Systems. 

* **Was es tut:** Herkömmliche Chatbots neigen oft dazu, Dinge zu „erfinden“ (sogenannte Halluzinationen). RAGFlow verhindert dies, indem es als sicheres **Gedächtnis** dient. 
* **Quellentreue:** Alle gesammelten Studien und Dokumente werden hier so aufbereitet, dass die KI bei jeder Frage exakt in den echten Dokumenten nachschlägt. Jede Antwort der simulierten Stakeholder wird dadurch direkt mit den zugrundeliegenden wissenschaftlichen Quellen und Zitaten belegt.

---

## 3. Automatisierte Erstellung der KI-Personas (Orchestrierung)
https://github.com/Shift-Institut-organization/RAGFlow-API-Client

Diese Komponente verbindet die Projektanforderungen mit den gesammelten Dokumenten in RAGFlow.

* **Rollenprofile erschaffen:** Aus den Projektvorgaben generiert das System maßgeschneiderte Anweisungen (System-Prompts) für die KI, die verschiedene Rollen definieren – zum Beispiel einen skeptischen Anwohner, eine Umweltexpertin oder einen Investor.
* **Dokumenten-Aufbereitung:** Die Quelldokumente werden intelligent aufgeteilt und in RAGFlow hochgeladen, damit die KI sie schnell und präzise durchsuchen kann.
* **Gruppendiskussion-Simulation:** Nutzerinnen und Nutzer können nacheinander mit verschiedenen Personas chatten. Da das System den bisherigen Gesprächsverlauf übergibt, entsteht der realistische Eindruck einer echten, interaktiven Gruppen- oder Podiumsdiskussion. Am Ende exportiert das System den gesamten Dialog mitsamt aller Quellen als übersichtlichen Bericht.

---

## 4. VR-Chat (Die interaktive Erfahrung)
*Dieser Bereich befindet sich konzeptionell in der Entwicklung und besitzt noch kein eigenes Code-Repository.*

* **Das Ziel:** Der VR-Chat bildet die Benutzeroberfläche für das finale Erlebnis. Statt nur rein textbasiert am Bildschirm zu chatten, soll hier eine immersive Umgebung geschaffen werden.
* **Erlebnis:** Nutzerinnen und Nutzer können sich in einer virtuellen oder interaktiven Umgebung bewegen und direkt mit den simulierten Stakeholdern in den Dialog treten.