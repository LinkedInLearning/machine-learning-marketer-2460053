# Anleitung zum Einrichten

<!-- TOC -->

* [Anleitung für Einsteiger](#fr-einsteiger)
    * [Kursmaterialien Herunterladen](#kursmaterialien-herunterladen)
    * [Python Installieren](#python-installieren)
    * [Eine Interactive Development Environment Installieren (Optional)](#eine-interactive-development-environment-installieren-optional)
    * [Ein Terminal öffnen und zu den Kursdateien Navigieren](#ein-terminal-ffnen-und-zu-den-kursdateien-navigieren)
    * [Einer virtuellen Umgebung (Virtual Environment) Erstellen](#einer-virtuellen-umgebung-virtual-environment-erstellen)
    * [Virtuelle Umgebung Aktivieren und Jupyter Notebooks Starten](#virtuelle-umgebung-aktivieren-und-jupyter-notebooks-starten)
* [Anleitung für Fortgeschrittene](#anleitung-fr-fortgeschrittene-setzt-voraus-dass-sie-python-und-git-bereits-installiert-haben)
    * [Kursmaterialien Herunterladen oder Klonen ](#kursmaterialien-herunterladen-oder-klonen)
    * [Eine virtuelle Umgebung Erstellen und Dependencies Installieren, und Jupyter Notebooks Starten](#eine-virtuelle-umgebung-erstellen-und-dependencies-installieren-und-jupyter-notebooks-starten)

<!-- TOC -->

# Anleitung für Einsteiger

### Kursmaterialien Herunterladen

- Gehen Sie nach [GitHub] (https://github.com/LinkedInLearning/machine-learning-marketer-2460053), klicken Sie auf den 
  grünen 'Code' und wählen Sie 'ZIP herunterladen'.
- Die Kursunterlagen werden als gezippter (zipped) Ordner mit dem Namen "machine-learning-marketer-2460053-main" an dem 
Ort heruntergeladen, an dem Sie den Computer angewiesen haben, sie herunterzuladen. Gehen Sie zu diesem Ort und entpacken 
Sie ('unzip') den Ordner. Entpacken Sie auch den Ordner OnlineRetail.csv an denselben Ort.
- Benennen Sie den Ordner um. Dies ist optional, macht die Anleitung aber einfacher. Ich werde das heruntergeladene 
Projekt umbenennen in 'ml_in_marketing' um; der Rest der Anleitung geht davon aus, dass dies Ihr Projektname ist.

### Python Installieren

Für die Entwicklung dieses Kurses wurde die Python-Version 3.7 verwendet, aber auch 3.8 und 3.9 sollten funktionieren. 
Bei Verwendung anderer Python-Versionen kann es zu Inkompatibilitäten sowohl im Kurscode als auch in dieser Anleitung 
geben, wenn Sie andere Python-Versionen verwenden. (Beachten Sie, dass Python-Versionen normalerweise drei Nummern haben
, z.B. 3.7.1, aber Sie können die dritte Nummer ignorieren; 3.7.1 reicht z.B. für 3.7).

- Auf Linux/MacOS ist normalerweise eine Version von Python 3.8.X installiert, die für dieses Projekt geeignet ist.
    - Wenn Sie aus irgendeinem Grund Linux/Mac OS verwenden und Python nicht installiert haben, finden Sie Anweisungen 
  zur Installation unter wiki.python.org] (https://wiki.python.org/moin/BeginnersGuide/Download). Dort finden Sie auch 
  einen Link zu der Seite mit den Python-Downloads auf python.org, wo Sie Ihr Betriebssystem auswählen können und zu 
  einer Liste von Python Downloads gelangen.
- Windows erfordert die Installation von [git](https://git-scm.com/) und 
[Python](https://www.python.org/downloads/windows/)
    - Ein hilfreicher Paketmanager für die Installation von Python unter Windows ist chocolatey. Sie können ihn anhand 
  der Anweisungen [hier](https://chocolatey.org/install) installieren (stellen Sie sicher, dass Sie das Terminal als 
  Administrator ausführen, wie es in der Anleitung heißt).
    - Dann können Sie chocolatey verwenden, um Python einzurichten. Verwenden Sie entweder
  ```choco install python --version=3.8.13``` (empfohlen) oder ```choco install python```, die die aktuellste Version von
  Python installiert.

Wie Sie feststellen können, welche Python-Version Sie haben (wenn überhaupt):

- Geben Sie ```python --version``` ein.

Wenn Sie eine andere Version als 3.7, 3.8 oder 3.9 haben, können Sie eine dieser Versionen mit Hilfe der oben 
aufgeführten Anweisungen installieren oben aufgeführten Anweisungen installieren.

### Eine Interactive Development Environment Installieren (Optional)

Es stehen verschiedene IDEs zur Verfügung, die alle ihre eigenen Installationsanweisungen enthalten. Ein einfacher 
Startpunkt ist Visual Studio Code: Es ist kostenlos, schnell und hat eine große Community mit Erweiterungen (Extensions) 
 und Funktionen hinter sich. PyCharm ist eine weitere beliebte Wahl, obwohl es eine Menge Funktionen hat und anfangs 
überwältigend sein könnte.

Wenn Sie mit einer IDE arbeiten möchten (optional für den nächsten kleinen Schritt, aber ansonsten überhaupt nicht 
erforderlich) und noch keine haben, dann schauen Sie bitte in den Online-Anleitungen für Ihrer IDE nach.

### Ein Terminal öffnen und zu den Kursdateien Navigieren

Je nachdem, ob Sie sich für eine IDE entschieden haben oder nicht, gibt es zwei Möglichkeiten, dies zu tun.

#### Option A: Über ein Computer Terminal or Visual Studio Code

Öffnen Sie ein Terminal auf Ihrem Computer (Sie können ein Terminal normalerweise wie jedes andere Programm öffnen oder 
im Internet nach der Verknüpfung für Ihr Betriebssystem suchen). Alternativ dazu können Sie Visual Studio Code öffnen 
und auf die Schaltfläche "Terminal" (in der oberen Menüleiste) klicken und "Neues Terminal" wählen.

Navigieren Sie zu dem Ort, an dem die Kursdateien gespeichert sind: Geben Sie dazu `cd` ein, gefolgt von einem 
Leerzeichen und dem Pfad zu dem Ordner, in dem die Dateien gespeichert sind. Der Pfad besteht aus allen Ordnern 
zwischen dem Ort, an dem Sie sich befinden, und dem Ort, zu dem Sie gehen müssen, getrennt durch einen `/` Slash
(Mac/Linux) oder einen `\` Backslash (Windows). Das Beispiel im nächsten Schritt geht davon aus, dass ich unter Mac OS 
arbeite und mein Terminal mein Benutzerverzeichnis "munro" öffnet, und dass sich in diesem Verzeichnis ein Ordner 
"Dokumente" befindet, in dem sich der Ordner mit den Kursmaterialien befindet. Sie müssen den Pfad entsprechend 
anpassen, und Sie sollten so lange navigieren bis zu dem Ordner, der die Datei "requirements.txt" enthält. Auch hier 
finden Sie Ressourcen online, die Ihnen helfen, wenn Sie nicht weiterkommen.

#### Option B: Über ein IDE

Starten Sie die IDE Ihrer Wahl. Ich verwende PyCharm für diese Anleitung, aber der Prozess für z.B. IntelliJ sollte 
ähnlich sein.

Wählen Sie "Datei" > "Öffnen" > navigieren Sie zu dem Ordner, der die Kursmaterialien enthält, z. B. "requirements.txt",
und klicken Sie auf "Öffnen". Wenn PyCharm Sie fragt, ob Sie dem Projekt vertrauen wollen, bestätigen sie dies! Wenn PyCharm
Sie fragt, wo Sie das Projekt öffnen wollen, wählen Sie "Neues Fenster".

Öffnen Sie ein Terminal innerhalb der IDE. Die Schaltfläche sollte sich entweder im Menü unten links oder im Menü oben 
links befinden, Wenn Sie sie nicht finden können, geben Sie Cmd+Umschalt+A (Mac) bzw. Strg+Umschalt+A (Windows) ein, um 
das Suchfeld "Aktionen" aufzurufen, und geben Sie dann 'Terminal' ein.

### Einer virtuellen Umgebung (Virtual Environment) Erstellen

Für die meisten Python-Projekte, die Sie von anderen erhalten, müssen Sie so genannte "Dependencies" herunterladen, 
d. h. die Python-Bibliotheken, die in dem Projekt verwendet werden. Diese Abhängigkeiten werden in einer Datei namens 
"requirements.txt" aufgeführt. Eine einfache (aber Warnung - falsch!) Weg, diese Abhängigkeiten zu installieren, ist es,
ein Terminal zu öffnen, zu dem Ort zu navigieren, an dem sich die Anforderungsdatei Datei sind, und 
`pip install -r requirements.txt` einzugeben (vorausgesetzt, Sie haben den Paketmanager 'pip' installiert). Das ist ein
großes Risiko: Wenn Sie später an anderen Python-Projekten arbeiten, können die Abhängigkeiten dieses Projekts mit dem, 
was Sie bereits installiert haben, inkompatibel sein.

Aus diesem Grund sollten Sie für jedes Ihrer Python-Projekte eine sogenannte "virtuelle Umgebung" erstellen. Der 
einfachste Weg dazu ist die Verwendung von pipenv. Hier sind alle Befehle, die Sie verwenden müssen (Sie können die 
erste Zeile überspringen, wenn Sie sie bereits im letzten Schritt ausgefüllt haben).

```bash
cd Documents/ml_in_marketing # Navigieren zu dem Ordner mit den Kursunterlagen (nicht notwendig, wenn Sie es bereits getan haben).
pip3 install pipenv # (oder pip install ...), Sie müssen dies nur einmal tun; wenn Sie in Zukunft neue Projekte mit neuen virtuellen Umgebungen starten, können Sie diese Zeile überspringen
pipenv install --python=3.8 -r requirements.txt
```

Nun müssen Sie einige Augenblicke warten, bis die virtuelle Umgebung erstellt und die Abhängigkeiten installiert werden.

### Virtuelle Umgebung Aktivieren und Jupyter Notebooks Starten

Sobald der letzte Schritt abgeschlossen ist, sollten Sie 'Successfully created virtual environment!' sehen.

Wenn Sie die Meldung 'Warning: Python 3.8 was not found on your system', bedeutet dies, dass pipenv keine Version von 
Python 3.8 auf Ihrem Computer finden konnte. Entfernen Sie zunächst die Umgebung mit `pipenv --rm`. Dann folgen Sie den 
Anweisungen in ['Python Installieren'](#python-installieren), um herauszufinden, welche Version Sie haben. Wenn Sie 
nicht 3.8 haben, können Sie es installieren und dann wieder von ```pipenv install --python=3.8 -r requirements.txt``` 
starten. Alternativ können Sie auch Ihre bestehende Version im Installationsbefehl verwenden, solange sie 3.7, 3.8 oder 
3.9 ist (ignorieren Sie die dritte Zahl in Ihrer Python-Systemversion, z.B. wenn Sie Python 3.9.1 haben, schreib einfach
3.9).

Wenn Sie vermuten, dass irgendetwas anderes fehlgeschlagen ist, können Sie die Umgebung mit `pipenv --rm` entfernen und 
erneut starten.

Sobald die virtuelle Umgebung erfolgreich erstellt wurde, können Sie sie aktivieren und Jupyter Notebooks in Ihrem 
Browser starten:

```bash
pipenv shell # Die virtuelle Umgebung aktivieren
jupyter notebook # Jupyter notebooks starten
```

Herzlichen Glückwunsch, jetzt können Sie loslegen!

Zum Schluss noch ein paar Tipps, wie Sie das Notebook schließen, die virtuelle Umgebung deaktivieren und zu einem 
späteren Zeitpunkt wieder aktivieren können später wieder aktivieren:

Strg+c im Terminal schließt ein Jupyter-Notizbuch (vergewissern Sie sich, dass Sie Ihr Notizbuch vorher im Browser 
gespeichert haben!) Nach werden Sie aufgefordert, ```y`` einzugeben, um zu bestätigen, dass Sie das Notizbuch schließen 
möchten.

```deactivate``` verlassen Sie die virtuelle Umgebung und kehren in das System zurück. Sie können dann den Terminal 
schließen.

Wenn Sie später wieder anfangen wollen, öffnen Sie das Terminal (auf Ihrem Computer oder in der IDE), navigieren Sie zu 
dem Ort des Projekts, geben Sie ```pipenv shell``` und erneut ```jupyter notebook``` ein.

# Anleitung für Fortgeschrittene (setzt voraus, dass Sie Python und Git bereits installiert haben)

### Kursmaterialien Herunterladen oder Klonen

- Gehen Sie zu [GitHub] (https://github.com/LinkedInLearning/machine-learning-marketer-2460053) und klonen Sie das 
Repository, oder laden Sie die Kursdateien herunter und entpacken Sie sie über die grüne Schaltfläche "Code".
- Benennen Sie den Ordner um. Dies ist optional, sorgt aber für einen schöneren Namen der virtuellen Umgebung (wenn Sie 
die Option pipenv install Option verwenden, die ich hier beschreiben werde). Ich benutze 'ml_in_marketing'.

### Eine virtuelle Umgebung Erstellen und Dependencies Installieren, und Jupyter Notebooks Starten

Wenn Sie Ihre eigene bevorzugte Methode haben, um eine virtuelle Umgebung zu erstellen und Dependencies zu installieren,
z.B. über ```pip install -r requirements.txt```, dann können Sie das gerne tun. Alternativ dazu finden Sie unten die 
Anweisungen für Verwendung von pipenv.

Öffnen Sie die IDE Ihrer Wahl oder die Terminal-App Ihres Computers und führen Sie die folgenden Befehle aus:

```bash
cd Documents/ml_in_marketing # Navigieren zu dem Ordner mit den Kursunterlagen
pip3 install pipenv # Wenn Sie pipenv noch nicht haben
pipenv install --python=3.8 -r requirements.txt # Sie können eine andere Python-Version wählen; 3.7-3.9 sollte funktionieren.
# Warten, bis der Vorgang abgeschlossen ist; es erscheint die Meldung 'Successfully created virtual environment!
pipenv shell # Die virtuelle Umgebung aktivieren
jupyter notebook # Jupyter notebooks started
# Wenn Sie mit der Arbeit fertig sind, verwenden Sie Strg+c, um das Notizbuch zu beenden (speichern Sie es vorher im Browser!).
deactivate # Die virtuelle Umgebung deaktivieren
```

- Pipenv scannt automatisch Ihr System und findet die erste brauchbare Python-Version, z.B. 3.8.
- Es gibt viele alternative Möglichkeiten, Python-Umgebungen zu verwalten:
    - conda (Anaconda, miniforge) oder mamba (schnellerer conda). Diese installieren strengere Binärdateien und arbeiten
  in der Regel zuverlässiger, sind aber langsamer (beim installierren) und brauchen mehr Speicherplatz 
      - virtualenv über verschiedene Hilfsskripte, die dasselbe tun wie pipenv, aber weniger intuitiv sind. Unten ist 
      ein Beispiel:

  ```bash
  virtualenv ml_in_marketing
  source ml_in_marketing/bin/activate
  pip install -r requirements.txt
  jupyter notebook
  # Ctrl+C to exit
  deactivate
  ```
