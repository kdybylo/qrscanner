# QRscanner – nasazení

Tato verze je rekonstrukce aplikace z konverzace, nikoli export původního CloudFront náhledu. Zachovává původní tmavý vzhled s tyrkysovými tlačítky.

## Zveřejnění
V repozitáři otevřete Settings → Pages. Zvolte Deploy from a branch, větev main a složku / (root), poté Save. Odkaz použijte až po úspěšném nasazení. HTTPS adresa očekávaná při výchozím nastavení: https://kdybylo.github.io/qrscanner/ .

## Funkce a omezení
- Generování textových, Wi-Fi a českých SPD platebních QR, export PNG.
- Generátor načítá qrcode-generator 1.4.4 z jsDelivr, potřebuje tedy internet a povolené CDN skripty. Obsah se generuje lokálně; QR hesla a platby se na CDN neodesílají. Samotné načtení skriptu je síťový požadavek.
- Skenování kamery a obrázků vyžaduje BarcodeDetector s podporou qr_code; není podporováno ve všech prohlížečích. Kamera vyžaduje zabezpečený kontext a souhlas uživatele.
- Odkazy http/https se otevírají až po stisku tlačítka; aplikace neověřuje důvěryhodnost cílového webu.
- Zobrazení Wi-Fi údajů a SPD plateb. EPC není implementováno.
- IBAN se kontroluje formátem a modulo 97; nejde o ověření vlastníka účtu ani bankovní autorizaci.
- Tato verze není offline PWA; nemá manifest, service worker ani PNG ikonu. Instalace jako aplikace není zaručena.
- Běh v konkrétním mobilním Chromu nebyl při přípravě ověřen. Po nasazení vyzkoušejte text, Wi-Fi se speciálními znaky, SPD, kameru, obrázek a otevření odkazu.
- LICENSE a README.md zůstávají beze změny.
