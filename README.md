## Readme zum Arbeiten an/mit dieser Website

In diesem Repository wird die Website zu Fab:UNIverse gepflegt. Fab:UNIverse ist eine Tagung für diejenigen, die im deutschsprachigen Raum an Hochschulen Fab Labs, Makerspaces, offene Werkstätten und ähnliche Orte betreiben oder betreiben wollen.  

- Der Content der Website wird unter [/docs](https://github.com/fabuniverse/website/tree/main/docs) geschrieben. 
- Die Website wird mit [MkDocs](https://www.mkdocs.org/) erzeugt
- [MkDocs-Material](https://squidfunk.github.io/mkdocs-material/) wird als Theme eingesetzt
- Wir nutzen bei Bedarf [MkDocs-Plugins](https://www.mkdocs.org/dev-guide/plugins/) zur Erweiterung. Im Moment verwenden wir nur [mkdocs-glightbox](https://blueswen.github.io/mkdocs-glightbox/) 
- Die Website wird nach jeder Änderung automatisch neu gebaut und als [GitHub-Page](https://pages.github.com/) veröffentlicht.


## Infos und How-to zum Arbeiten mit der Website

Wer etwas an der Website ändern möchte, kann einfach auf der veröffentlichten [Website](https://fab-universe.de) auf den "Edit-Button" drücken, der sich auf jeder Seite oben rechts befindet. Alternativ kann man auch direkt in der Ordnerstruktur des Git-Repositories die jeweilige Markdown-Datei unter [/docs](https://github.com/fabuniverse/website/tree/main/docs) bearbeiten. 

### Ordnerstruktur der Website

#### Für den Alltag wichtig

/docs = Quelldateien der Website. Hier liegen die einzelnen "Pages" oder "Seiten" unserer Website. `2017.md` z.B. ist die [Seite der Fab:UNIverse 2017](https://fabuniverse.github.io/website/2017/). Verlinkungen von einer .md-Datei auf eine andere funktionieren so: `[LINKNAME](DATEINAME.md)`.

/docs/images = Hier werden Fotos und Videos gespeichert. Verlinkungen von den .md-Dateien aus /docs funktioniert so: `![LINKNAME](images/DATEINAME.jpg)` 

mkdocs.yml = Konfigurationsdatei für Mkdocs. Hier werden allgemeine Optionen für die Website festgelegt, Plugins geladen und - wichtig für den Alltag - die **Navigation** der Website konfiguriert. 


#### Weitere Unterordner unter /docs

/docs/stylesheets = CSS für gestalterische Anpassungen. Braucht man im Alltag nicht.

/docs/dateien = Ordner für PDFs und andere Dateien, die keine Medien sind


#### Einzelne Dateien

.gitignore = Git-Konfiguration. Für den Alltag unwichtig

LICENSE.md = Lizenz-Informationen

README.md = Diese Datei


### Infos zu Mkdocs & Markdown

Die typischen Web-"Programmier-Sprachen" sind HTML, CSS und Javascript. Da die wenigsten diese drei Sprachen eben mal so beherrschen, benutzt diese Website ein Tool namens [mkdocs](https://mkdocs.org), um die Arbeit an der Website zu vereinfachen. 

Mkdocs ist *kein* Content-Management-System (CMS) wie Wordpress o.Ä., sondern (nur) ein Tool zum vereinfachten Erzeugen statischer Websiten ("Static Website Generator"). Eine statische Website benötigt nur einen minimalen Web-Server um dauerhaft und frei von Wartung und Updates existieren zu können. Eine dynamische Website (z.B. jedes CMS) hingegen kann zwar viele komplexere schöne Dinge (z.B. Nutzer\*Innen- und Rechteverwaltung, Backend zum Einloggen für Autor\*Innen, usw) - braucht dafür aber zwangsläufig serverseitig viel mehr permanent laufende und zu wartende Infrastruktur. Ohne permanente Wartung und Updates "zerbröseln" dynamische Websiten über die Jahre und werden unsicherer. 

Statische Websites haben außerdem den Vorteil, dass man sie über Dienste wie [Github Pages](https://pages.github.com/) oder [GitLab Pages](https://docs.gitlab.com/ee/user/project/pages/) kostenfrei veröffentlichen kann, während dynamische Websites im Normalfall durch eigene/gemietete Server-Infrastruktur laufende Kosten verursachen. 

Mkdocs und seine diversen Plugins (wie [MkDocs-Material](https://squidfunk.github.io/mkdocs-material/)) sind also Tools, die aus einfachem Text und einigen Sonderzeichen HTML, CSS und Javascript bauen. Die Sprache, die mkdocs erkennt und umsetzen kann, heißt [Markdown](https://t3n.de/news/eigentlich-markdown-478610/) und ist im Web sehr verbreitet. 

Markdown ist eine vereinfachte Auszeichnungssprache, die es ermöglicht, Texte mit einfacher Syntax zu formatieren. Entwickelt wurde sie, um die Lesbarkeit zu maximieren und gleichzeitig zu ermöglichen, dass der Text als HTML veröffentlicht werden kann. 

Übrigens lässt sich Markdown mit Tools wie [Pandoc](https://pandoc.org) auch leicht in LaTeX, Word, PDF, Powerpoint und diverse andere Sprachen / Formate übersetzen. Alternativen zu Pandoc mit etwas mehr grafischem Interface sind z.B. [PandocGUI](https://github.com/Ombrelin/pandoc-gui) oder [Marked](https://marked2app.com/). Kombiniert man dann noch z.B. LaTeX mit [Github Actions](https://github.com/features/actions), lassen sich völlig automatisiert und kostenfrei in der Cloud aus ein und demselben Markdown-Quelldokument nicht nur Websites wie unsere Fab:UNIverse-Seite erzeugen und veröffentlichen, sondern auch PDFs, Skripte, Word-Dokumente und vieles mehr.

#### Markdown-Beispiele

- **Überschriften**: Mit `# ` können Überschriften erzeugt werden. Umso mehr `#` genutzt werden, desto kleiner wird die Überschrift. Die erste Überschrift `Readme zum Arbeiten an/mit dieser Website` sieht in Markdown z.B. so aus `##  Readme zum Arbeiten an/mit dieser Website`.

- **Zeilenumbruch**: Zwei Leerzeichen am Ende einer Zeile erzeugen einen Zeilenumbruch.

- **Textformatierung**: Text kann als *kursiv* (`*kursiv*`), **fett** (`**fett**`) oder `monospace` (\``monospace`\`) formatiert werden.

- **Listen**: Listen können mit `- ` (nicht nummerierte Listen) oder `1. ` (nummerierte Listen) zu Beginn eines jeden Listenpunktes erstellt werden.

- **Links**: Dieser Link [FabUNI:verse-Website](https://fab-universe.de), der zu unserer Website führt, sieht in Markdown so aus: `[FabUNI:verse-Website](https://fab-universe.de)`. Also der Name des Links, der auf der Website erscheinen soll, in eckigen Klammern und die Link-Adresse direkt dahinter in runden Klammern.

- **Markdown ignorieren**: Manchmal ist es notwendig, dass die Zeichen, die Markdown-technisch Dinge auslösen, dies nicht tun, da Ihr sie so anzeigen möchtet. Z.B beim Gendern mit `*` kann es vorgekommen, dass das Sternchen als kursiv-Marker verstanden wird. Dies könnt Ihr vermeiden, indem Ihr ein `\` vor andere Zeichen setzt. Also z.B. `Mitarbeiter\*innen` wird angezeigt als Mitarbeiter\*innen. Was wenn Ihr nun aber `\` als Zeichen braucht? Dann könnt Ihr das so lösen `\\`. Das wird angezeigt als \\.

#### Website-spezifisches Markdown

Während das Markdown weiter oben "gängiges" Markdown ist, gibt es auch Markdown, das entweder nur über mkdocs oder über eigene Einstellungen von uns funktioniert. 

- **Bilder**: Bilder könnt Ihr ähnlich wie Links einbinden: `![BILD-BESCHREIBUNG](medien/NAME.jpg)`. `BILD-BESCHREIBUNG` ist der alternativ-Text, der angezeigt wird, wenn das Bild nicht angezeigt werden kann, oder von Screen-Readern für Menschen mit Sehbeeinträchtigung vorgelesen wird. `images` ist der Ordner unserer Website, in dem wir alle Bilder und Videos speichern, die auf der Website angezeigt werden. Der `/` zeigt an, das wir eine Datei meinen, die in dem medien-Ordner liegt. `NAME.jpg` muss dann natürlich durch den eigentlichen Dateinamen ersetzt werden. 

- **Verlinkungen auf Unterpunkte einer Seite**: Sagen wir Ihr möchtet auf einer Seite, die sehr lang ist, direkt auf einen Unterpunkt dieser Seite verweisen, dann geht das folgendermaßen:  
`## UNTERPUNKT {: #SINNVOLLERNAME }`
Die Anzahl der `#` spielt hier keine Rolle. `UNTERPUNKT` ist hier die Überschrift, zu der Ihr direkt verlinken möchtet. `{: #SINNVOLLERNAME }` setzt Ihr hinter die entsprechende Überschrift und ersetzt `SINNVOLLERNAME` durch einen intuitiven Titel. Vermeidet dabei wie immer Sonderzeichen, Umlaute oder Leerzeichen. Dadurch habt Ihr nun sozusagen mkdocs erklärt, dass es dort einen Ankerpunkt setzen soll, auf den Ihr von überall her verlinken könnt. 
Verlinkungen von der selbe Seite sehen dann so aus: `[LINKNAME](#SINNVOLLERNAME)`
Verlinkungen von anderen Seiten: `[LINKNAME](SEITENNAME.md#SINNVOLLERNAME)`  
`LINKNAME`: Name des Links der angezeigt werden soll.  
`#SINNVOLLERNAME`: Der Name, den ihr Eurem "Anker" gegeben habt.  
`SEITENNAME`: Name der .md-Datei auf deren Unterpunkt Ihr verlinken möchtet. 

- **Weitere Möglichkeiten**: Weitere Möglichkeiten, die Website mit Markdown zu gestalten, findet Ihr in der Dokumentation von [Mkdocs Material](https://squidfunk.github.io/mkdocs-material/reference/).  
Hier z.B. die [hervorgehobenen Infoblöcke](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)  