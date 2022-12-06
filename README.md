# Siton210
ESPhome kód pro čtení dat přes Modbus z MPPT měniče Siton210

Zařízení, ze kterého jsou získávána data:
Fotovoltaický MPPT měnič pro ohřev vody SITON 210
http://tnweb.tode.cz/fotovoltaicky-mppt-menic-pro-ohrev-vody-siton-210/

Zařízení, pomocí kterého jsou data čtena (Siton WiFi modul):
http://tnweb.tode.cz/odesilani-dat-ze-sitonu-na-emoncms-pres-wifi/
Jednoduše použijte uvedené schéma zapojení. Není potřeba provádět žádné technické úpravy, pouze nenahrávejte uvedený firmware pro komunikaci s Emoncms.

Postup:
1. Postavte Siton210 (nemusíte osazovat DPS pro RS485)
2. Postavte Siton WiFi modul
3. V menu Siton210 nastavte druh komunikace na Modbus
4. V menu Siton210 nastavte ID měniče/adresu. Výchozí adresa je 12 (0x0C).
5. V ESPhome (v Home Assistant) upravte kód podle potřeby (např. nastavte stejnou adresu měniče nebo změňte název zařízení). Většinu potřebných změn provedete hned na začátku kódu v části substitutions.
6. Do ESPhome kódu doplňte Home Assistant API key, heslo pro OTA aktualizace a vytvořte vlastní heslo pro WiFi Fallback Hotspot. Využijte připravené hesla, které generuje ESPhome při vytvoření nového zařízení.
7. Nahrajte kód do Siton WiFi modulu
