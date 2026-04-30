============================================================
  Fågelobservationer Västerbotten – Installationsguide
============================================================

KRAV
----
• Python 3.8 eller nyare  (https://www.python.org/downloads/)
• Ett gratis konto på artportalen.se / SLU
  (Skapa konto: https://useradmin.slu.se/skapa-konto)


SNABBSTART (3 steg)
-------------------

1. Installera Python-beroenden (kör EN gång):
   Öppna ett terminalfönster (cmd / PowerShell) i den här mappen och kör:

       pip install flask flask-cors requests

2. Starta proxyn:

       python proxy.py

   Du bör se:
       🦅  Fågelobservationer Västerbotten – Lokal proxy
          Lyssnar på: http://localhost:5050

3. Öppna faglar-vasterbotten.html i din webbläsare.
   Klicka på "Logga in" (gul rad längst upp) och ange ditt SLU-konto.


UTAN PROXY (ingen installation)
--------------------------------
Du kan också öppna faglar-vasterbotten.html direkt utan att starta proxyn.
Appen visar då data från GBIF (ca 2 månaders fördröjning mot artportalen).


VALFRITT – Prenumerationsnyckel
--------------------------------
En prenumerationsnyckel ger bättre API-kvot (fler anrop per dag).
Den är INTE nödvändig för att komma igång.

Om du vill ha en:
1. Gå till https://api-portal.artdatabanken.se
2. Logga in med ditt SLU-konto
3. Prenumerera på produkten "Species Observations – multiple data resources"
4. Kopiera din prenumerationsnyckel och klistra in den i inloggningsformuläret


FELSÖKNING
----------
Problem: "Inloggning misslyckades"
  → Kontrollera e-post och lösenord (samma som artportalen.se)
  → Prova att logga in på artportalen.se i webbläsaren för att verifiera

Problem: "Kunde inte nå proxyn"
  → Se till att proxy.py körs (steg 2 ovan)
  → Kontrollera att port 5050 inte blockeras av brandvägg

Problem: Listan är tom (vid live-läge)
  → Prova ett annat datum – det kan saknas rapporter just det datumet
  → Kontrollera terminalen för felmeddelanden från proxy.py


FILER
-----
faglar-vasterbotten.html  – Webbappen (öppna i webbläsaren)
proxy.py                  – Lokal proxyserver (starta med Python)
requirements.txt          – Python-beroenden
README.txt                – Den här filen
============================================================
