---
type: slide
slideOptions:
  transition: slide
  theme: white
---

<style>

.left {
  text-align: left !important;
}

</style>

# Willkommen beim

<img style="border:unset;background:unset;box-shadow:unset;" src="./nixos-hires.png" width="500px" alt="logo" />

# workshop

---

## Requirements

<ul>
  <li class="left fragment">(etwas) Linux Erfahrung</li>
  <li class="left fragment">Lust neues kennen zu lernen</li>
  <li class="left fragment">Eine Plattform für die NixOS Installation
    <ul>
      <li class="left fragment">am besten einen Laptop/Hardware</li>
      <li class="left fragment">VM ist auch vollkommen in Ordnung</li>
      <li class="left fragment">Cloud-Instanz?</li>
    </ul>
  </li>
</ul>

---

## Theorie

Nix ist eine "special snowflake"

<div class="fragment">wie auch das Logo zeigt...</div>

----

## Begriffe

<ul>
  <li class="left fragment">Nix
    <ul>
      <li class="left fragment">Programmiersprache</li>
      <li class="left fragment">Package-Manager</li>
      <li class="left fragment">"Compiler" oder "Templating Engine"</li>
      <li class="left fragment">Die Lösung für all eure Probleme</li>
    </ul>
  </li>
  <li class="left fragment"><a href="https://github.com/nixos/nixpkgs">Nixpkgs</a></li>
  <li class="left fragment">NixOS - Betriebssystem</li>
  <li class="left fragment">Packages - Softwarepakete</li>
  <li class="left fragment">Derivations - "Bauanleitungen"</li>
</ul>

----

## Tolle Features von Nix

## Reproduzierbarkeit

<li class="left fragment">Alle Files sind kryptographisch verifizierbar</li>
<li class="left fragment">Dependencies werden gehashed</li>
<li class="left fragment">...können also klar identifiziert werden</li>
<li class="left fragment">Nix ist funktional</li>

---

## Vergleich mit APT

| Operation          | Ubuntu               | NixOS    | Nix |
| ----               | -----                | -------- | --- |
| Paket installieren | sudo apt install vim |          |     |

