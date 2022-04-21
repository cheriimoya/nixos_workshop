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

<img style="border:unset;background:unset;box-shadow:unset;" src="/media/nixos-hires.png" width="500px" alt="logo" />

# Workshop

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
<div class="left fragment">In diesem Workshop nur 64Bit "Hardware"</div>

---

## Theorie

Nix ist eine "special snowflake"

<div class="fragment">wie auch das Logo zeigt...</div>
<div class="fragment"><img style="margin-top:1em;border:unset;background:unset;box-shadow:unset;" src="/media/snowflake.png" width="150px" alt="logo" /></div>

----

### Begriffe

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

---

### Tolle Features von Nix

----

### Sauberes Dependency-Management

<ul>
<li class="left fragment">Mehrere Versionen der gleichen Library</li>
<li class="left fragment">Dependencies werden gehashed</li>
<li class="left fragment">...können also klar identifiziert werden</li>
<li class="left fragment">...sind somit immer "komplett"</li>
</ul>

----

### Reproduzierbarkeit

<ul>
<li class="left fragment">Nix ist funktional</li>
<li class="left fragment">Alle Files sind kryptographisch verifizierbar</li>
<li class="left fragment">Eine Derivation gibt auf jedem System den gleichen Output</li>
</ul>

----

### Sprachenunabhängig

Es ist egal ob man
<ul>
<li class="left fragment">Python</li>
<li class="left fragment">C/C++</li>
<li class="left fragment">Go</li>
<li class="left fragment">Rust</li>
<li class="left fragment">Java</li>
<li class="left fragment">Javascript</li>
<div class="fragment">oder Sonstiges verwendet</div>
</ul>

----

### Multi-User Support

<li class="left fragment">Verschiedene (nicht root) User können Software installieren</li>
<li class="left fragment">Keine Konflikte durch komplette Dependencies</li>

----

### Atomic-Updates und Rollbacks

<li class="left fragment">Einzelne Pakete können geupdated werden</li>
<li class="left fragment">Und auch wieder downgraded werden</li>

----

### Binary als auch From-Source Package-Management

Es gibt sowohl einen binary cache als auch die Option Pakete from source zu bauen

---

## NixOS

Es gibt ein `configuration.nix` file in dem die gesamte Systemkonfiguration festgehalten ist.

----

### Beispiel

```nix
{ config, pkgs, ... }: {
  imports = [ ./hardware-configuration.nix ];

  # (for BIOS systems only)
  boot.loader.grub.device = "/dev/sda";

  environment.systemPackages = with pkgs; [
    emacs vim
  ];

  # Enable the OpenSSH server. Duh!
  services.sshd.enable = true;
}
```

----

### Optionen und Packages

Was für Optionen und Packages gibt es?

<div class="fragment">Die findet man unter der <a href="https://search.nixos.org/options">NixOS search</a></div>

---

## Getting Started

----

### Installation

ISOs von der [NixOS download Seite](https://nixos.org/download)

- [minimal](https://channels.nixos.org/nixos-21.11/latest-nixos-minimal-x86_64-linux.iso)
- [gnome](https://channels.nixos.org/nixos-21.11/latest-nixos-gnome-x86_64-linux.iso)
- [plasma](https://channels.nixos.org/nixos-21.11/latest-nixos-plasma5-x86_64-linux.iso)

<div class="fragment">Danach nach <a href="https://nixos.org/manual/nixos/stable/index.html#ch-installation">der Anleitung</a> vorgehen</div>

---

## Und jetzt?

<li class="left fragment">Auch mal ins <a href="https://nixos.org/manual/nixpkgs/stable/index.html">Nixpkgs Manual</a> schauen</li>
<li class="left fragment"><a href="https://nix.dev/tutorials/ad-hoc-developer-environments">Nix shells</a> anschauen</li>
<li class="left fragment">Spaß haben und bei Problemen <s>mich</s>die <a href="https://nixos.org/manual/nixos/stable/#preface">Community</a> fragen</li>

---

## CC-Attribution

Logo designed by Tim Cuthbertson (<a href="https://github.com/timbertson">@timbertson</a>)
