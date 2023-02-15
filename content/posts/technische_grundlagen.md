---
title: "01 Technische Grundlagen"
date: 2023-02-15T09:45:35Z
draft: false
toc: true
---
Der Kurs wird eingeleitet mit den technischen Grundlagen ein, welche bei der Durchführung des Kurses verwendet werden. 
Die Unterlagen im Kurs werden in [HedgeDoc](https://hedgedoc.org/) zur Verfügung gestellt. Damit können die Studierenden
selber direkt diese bearbeiten und alle sehen diese Änderungen.

Gemeinsames Dokument: [Link](https://pad.gwdg.de/Nj7bLYj_QHqaP9o29V0yGw?both)

Zum Anfang gab es eine Einführung in den Kurs selber und was das Ziel ist. Diese Einleitung hat einen guten Überblick gegeben. 
Anschliessend haben wir den Rest der Grundlagen betrachtet mit Markdown, GitHub, Codespaces, Unix Shell und Git.
Alle diese Themen sind Teil meines Arbeitsalltags ausser der Codespaces auf GitHub. Diesen hatte ich noch nicht verwendet, da wir
eher auf GitLab unterwegs sind.

Mein Fokus war auf dem Aufsetzen der Webseite für diese Lerntagebuch und die Umgebung dafür. Da Codespaces vorgestellt wurden,
habe ich mich dazu entschieden dies auch zu verwenden. Es macht auch ein paar Sachen einfacher. Visual Studio Code ist auch ein
sehr guter Editor den ich für verschiedene Projekte verwende. Der Vorteil ist, dass es sehr schnell ist und es unendlich viele 
Möglichkeiten zu erweitern. Der Nachteil ist, dass die viele Teile oft nicht so einfach zusammenpassen und man regelmässig 
manuell nachbessern muss mit den Konfiguration, damit alles funktioniert.

Für das Lerntagebuch verwende ich [Hugo](https://gohugo.io/). Dies ist ein Static Site Generator (SSG) der frei Verfügbar ist. Basiert 
auf der Programmiersprache Go und verwendet Markdown als default Inhaltssprache. Diese macht es sehr einfach, schnell eine Umgebung
aufzubauen und die Seiten zu publizieren.

Die Webseite wird auf GitHub Pages publiziert mit der Hilfe von GitHub Actions. Das heisst, dass gesamte Projekt 
kann direkt auf GitHub gemacht werden ohne eine andere Platform verwenden zu müssen.

Das Einrichten des Codespaces war Grundsätzlich sehr einfach, hatte aber dennoch ein zwei Hiccups. Ich habe verschiedene Tutorials verwendet
um die aktuelle Umgebung aufzubauen.

Die erste Google suche hat mir einen Blog-Artikel geliefert, der mich in der ersten Hälfte unterstütz hat: [Blog](https://shotor.com/blog/build-a-hugo-static-site-in-your-browser-using-github-codespaces/). In diesem Blog wird die erste Umgebung für Hugo und mit einem einfachen Theme aufgebaut. 
Das Theme ist dafür verantwortlich wie die resultierende Webseite aussieht und was es für Features in der Seite hat. Dieses einfache Theme hat den Vorteil, dass man kaum denken muss und ein einfaches modernes Design hat für einen Blog.

Im zweiten Teil dieses Tutorials sollte die Seite auf [Netifly](https://www.netlify.com/) publiziert werden. Das wollte ich nicht tun, da es auch einfach
möglich ist das gleiche direkt auf GitHub zu machen.

Deshalb habe ich dann nach einer Alternativen gesucht und bin schnell fündig geworden in der offiziellen Dokumentation (über Google) wie man eine GitHub Page einrichten kann mit GitHub Actions. Das heisst, dass die Seite jedes mal, wenn ich neuen Code pushe automatische gebaut und publiziert wird. 
Diese zweite [Tutorial](https://gohugo.io/hosting-and-deployment/hosting-on-github/) hat zwar eine GitHub Actions Konfiguration, diese hat aber bei einem ersten Versuch für mich nicht funktioniert. Deshalb habe ich nach noch einer alternative Gesucht. Dabei kam ich auf die Settings von GitHub Pages, wo man direkt einen GitHub Action workflow aus einem Template auswählen kann und einbauen kann. Es hat auch tatsächlich ein Hugo Template direkt als Featured Content. Dementsprechend war das einfach. Nur leider hat auch das zuerst nicht geklappt. Ich musst einen Schritt im Bauprozess der nicht funktioniert hat löschen.

Damit hatte ich nun eine funktionierende Webseite publiziert und konnte mit dem Verfassen des Tagebuchs beginnen!

# Wichtige Links

- Hugo Dokumentation: https://gohugo.io/
- Hosting on GitHub: https://gohugo.io/hosting-and-deployment/hosting-on-github/
- Hugo in Codespaces: https://shotor.com/blog/build-a-hugo-static-site-in-your-browser-using-github-codespaces/
- Hugo Github Action: https://github.com/marketplace/actions/hugo-setup
- Ananke Docs: https://themes.gohugo.io/themes/gohugo-theme-ananke/
- Ananke Demo: https://gohugo-ananke-theme-demo.netlify.app/