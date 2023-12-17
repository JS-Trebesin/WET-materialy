# Git - příkazy

### Instalace a nastavení ⚙️🔧

<table>
  <tr>
    <td><strong>git --version</strong></td>
    <td>Ověření instalace a verze Gitu</td>
  </tr>
  <tr>
    <td><strong>git config --global user.name "jméno"</strong></td>
    <td>Nastavení uživatelského jména</td>
  </tr>
  <tr>
    <td><strong>git config --global user.email "email@trebesin.cz”</strong></td>
    <td>Nastavení emailové adresy</td>
  </tr>
</table>

### Tvorba a klonování repozitáře 🆕🐑

<table>
  <tr>
    <td><strong>git init</strong></td>
    <td>Inicializace (vytvoření) nového Git repozitáře</td>
  </tr>
  <tr>
    <td><strong>git branch -m master main</strong></td>
    <td>Přejmenuje hlavní větev z master na main (Github používá main pro hlavní větev)</td>
  </tr>
  <tr>
    <td><strong>git clone &lt;adresa&gt;</strong></td>
    <td>Naklonuje repozitář z internetu</td>
  </tr>
</table>

### Informace o repozitáři ℹ️🔍

<table>
  <tr>
    <td><strong>git status</strong></td>
    <td>Vypíše informace o našem repozitáři a souborech</td>
  </tr>
  <tr>
    <td><strong>git log</strong></td>
    <td>Zobrazí historii commitů</td>
  </tr>
  <tr>
    <td><strong>git diff</strong></td>
    <td>Zobrazí rozdíly mezi soubory</td>
  </tr>
</table>

### Práce se soubory (Staging area - přípravná fáze) 🗂️✅

<table>
  <tr>
    <td><strong>git add &lt;název_souboru&gt;</strong></td>
    <td>Přidá soubor (nebo složku) do staging area</td>
  </tr>
  <tr>
    <td><strong>git add .</strong></td>
    <td>Přidá všechny soubory do staging area</td>
  </tr>
  <tr>
    <td><strong>git commit -m "zpráva”</strong></td>
    <td>Commitne (provede a uloží) změny se zprávou</td>
  </tr>
  <tr>
    <td><strong>git commit -am “zpráva”</strong></td>
    <td>Kombinace příkazů git add. + git commit -m → vše přidá a commitne</td>
  </tr>
  <tr>
    <td><strong>git restore --staged &lt;název_souboru&gt;</strong></td>
    <td>Odstraní soubor ze staging area</td>
  </tr>
</table>

### Větvení (branching) 🌳🍴

<table>
  <tr>
    <td><strong>git branch</strong></td>
    <td>Seznam všech větví (branches)</td>
  </tr>
  <tr>
    <td><strong>git branch &lt;název_větve&gt;</strong></td>
    <td>Vytvoří novou větev (branch)</td>
  </tr>
  <tr>
    <td><strong>git switch &lt;název_větve&gt;</strong></td>
    <td>Přepne se na jinou větev (branch)</td>
  </tr>
  <tr>
    <td><strong>git merge &lt;název_větve&gt;</strong></td>
    <td>Sloučí změny ze zadané větve do aktuální větve - lze sloučit změny i ze vzdálené větve na internetu</td>
  </tr>
  <tr>
    <td><strong>git restore &lt;název_souboru&gt;</strong></td>
    <td>Vrátí změny z posledního commitu</td>
  </tr>
</table>

### Vzdálené repozitáře 🌍☁️

<table>
  <tr>
    <td><strong>git remote add &lt;název&gt; &lt;URL&gt;</strong></td>
    <td>Přidá nový vzdálený repozitář a pojmenuje jej (v 99% případů používáme pro název slovo <strong>origin</strong>)</td>
  </tr>
  <tr>
    <td><strong>git remote -v</strong></td>
    <td>Zobrazí seznam vzdálených repozitářů</td>
  </tr>
  <tr>
    <td><strong>git push &lt;vzdálený_repo&gt; &lt;větev&gt;</strong></td>
    <td>Pošle změny do vzdáleného repozitáře</td>
  </tr>
  <tr>
    <td><strong>git fetch &lt;vzdálený_repo&gt;</strong></td>
    <td>Stáhne změny ze vzdáleného repozitáře </td>
  </tr>
  <tr>
    <td><strong>git pull &lt;vzdálený_repo&gt; &lt;větev&gt;</strong></td>
    <td>Stáhne a sloučí změny ze vzdáleného repozitáře -> pull je kombinace git fetch + git merge</td>
  </tr>
</table>

### Pokročilejší příkazy 🧙‍♂️🚀

<table>
  <tr>
    <td><strong>git stash</strong></td>
    <td>Dočasně uloží změny do stashe (do "skrýše")</td>
  </tr>
  <tr>
    <td><strong>git stash pop</strong></td>
    <td>Obnoví změny ze stashe</td>
  </tr>
  <tr>
    <td><strong>git commit --amend</strong></td>
    <td>Upraví poslední commit</td>
  </tr>
  <tr>
    <td><strong>git revert &lt;hash_commitu&gt;</strong></td>
    <td>Vytvoří nový commit, který obnoví změny ze zadaného commitu</td>
  </tr>
  <tr>
    <td><strong>git checkout</strong></td>
    <td>Git checkout je kombinací git switch a git restore - zvládá funkce obou těchto příkazů</td>
  </tr>
  <tr>
    <td><strong>git checkout &lt;větev&gt;</strong></td>
    <td>Funguje stejně jako git switch, přepne se na danou větev</td>
  </tr>
  <tr>
    <td><strong>git checkout -- &lt;název_souboru&gt;</strong></td>
    <td>Funguje jako git restore - vrátí změny z posledního commitu</td>
  </tr>
  <tr>
    <td><strong>git checkout &lt;hash_commitu&gt;</strong></td>
    <td>Umožní zobrazit stav souboru v době daného commitu</td>
  </tr>
</table>
