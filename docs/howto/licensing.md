# 📜 Licensing

The licensing it's a fundamental phase of a software project.
There are many misconception, about software licensing and copyrighting but at Dyne.org we 
are 🥷-fu of Open source and Free software and licensing is our bread and butter.

Now without further dwelling, for pragramtic developers we use a tool to handle
source files **[reuse tool](https://reuse.software/)**.

Main benefits:
 1. FSFE offically supported
 1. Honours .gitignore
 1. Add headers automatically
 1. Uses [SPDX License List](https://spdx.org/licenses/)
 1. Generates SBOM (Software Bill Of Materials)
 1. Downloads all the needed LICENSE files

Most of our software is under Affero GPL 3 license that is identified by the `AGPL-3.0-or-later` SPDX identifier.

## 🕹️ Let's get our hands dirty


### TL;DR

```bash
reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi Azizi <puria@dyne.org>" --license="CC0-1.0" .gitignore yarn.lock
reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi Azizi <puria@dyne.org>" --license="CC-BY-NC-SA-4.0" static/* 
reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi Azizi <puria@dyne.org>" --license="AGPL-3.0-or-later" <all the other files and directories>
reuse download --all
git add .
git commit -am "license: add reuse compliancy and licensing the software"
reuse lint
```

### Initialize the repo

```bash::6,10,14,21,24,27,30
$ reuse init
Initializing project for REUSE.

What license is your project under? Provide the SPDX License Identifier.
To stop adding licenses, hit RETURN.
AGPL-3.0-or-later

What other license is your project under? Provide the SPDX License Identifier.
To stop adding licenses, hit RETURN.
CC-BY-NC-SA-4.0

What other license is your project under? Provide the SPDX License Identifier.
To stop adding licenses, hit RETURN.
CC0-1.0

What other license is your project under? Provide the SPDX License Identifier.
To stop adding licenses, hit RETURN.


What is the name of the project?
Luigi van der Dyne

What is the internet address of the project?
https://luigi.dyne.org

What is the name of the maintainer?
Puria Nafisi Azizi

What is the e-mail address of the maintainer?
puria@dyne.org

All done! Initializing now.

Downloading AGPL-3.0-or-later
LICENSES/AGPL-3.0-or-later.txt already exists
Downloading CC-BY-NC-SA-4.0
Downloading CC0-1.0

Creating .reuse/dep5

Initialization complete. 
```

### Add headers to all files

Use the licenses as below:
* CC0-1.0 for insignificant files (means actually public domain) eg. .gitignore file
* CC-BY-NC-SA-4.0 for contents and medias and or whatever artwork that is not actual code
* AGPL-3.0-or-later for the code and the rest files part of the software

Let's add for instance the CC0 to the .gitignore file:

```bash
$ reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi Azizi <puria@dyne.org>" --license="CC0-1.0" .gitignore

Successfully changed header of .gitignore
```

Now let's add the binary file images with the Creative Commons like:

```bash
reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi A zizi <puria@dyne.org>" --license="CC-BY-NC-SA-4.0" static/* 
Successfully changed header of static/02_howto.png.license
Successfully changed header of static/Twitter post - 64.svg.license
Successfully changed header of static/Twitter post - 97.svg.license
Successfully changed header of static/01_howto.png.license
```

And now all the other files as the main sources,

```
reuse annotate --copyright="Dyne.org foundation" --copyright="Puria Nafisi A
zizi <puria@dyne.org>" --license="AGPL-3.0-or-later" .github/workflows/deploy.yml README.md ecosystem.co
nfig.js mechanic.config.js

Successfully changed header of .github/workflows/deploy.yml
Successfully changed header of ecosystem.config.js
Successfully changed header of README.md
Successfully changed header of mechanic.config.js
```

### Download all the LICENSE files

Download/Update all the license files that should be present in the repo

```
reuse download --all
```


### Check that everithing is ok

```
reuse lint
```

## 📹 Some intro video

<video controls="controls" poster="/img/poster.jpg" crossorigin="crossorigin">
  <source src="https://download.fsfe.org/videos/reuse/reuse_software_en_desktop.mp4" type="video/mp4; codecs=&quot;avc1.42E01E, mp4a.40.2&quot;" media="screen and (min-device-width:1000px)">
  <source src="https://download.fsfe.org/videos/reuse/reuse_software_en_desktop.webm" type="video/webm; codecs=&quot;vp9, opus&quot;" media="screen and (min-device-width:1000px)">
  <source src="https://download.fsfe.org/videos/reuse/reuse_software_en_mobile.mp4" type="video/mp4; codecs=&quot;avc1.42E01E, mp4a.40.2&quot;" media="screen and (max-device-width:999px)">
  <source src="https://download.fsfe.org/videos/reuse/reuse_software_en_mobile.webm" type="video/webm; codecs=&quot;vp9, opus&quot;" media="screen and (max-device-width:999px)">

  <track src="https://download.fsfe.org/videos/reuse/subtitles/webvtt/reuse_en.vtt" kind="subtitles" srclang="en" label="English">
</video>

## 🌐 Further links and bibliography

* https://spdx.dev/
* https://reuse.software/
* 
