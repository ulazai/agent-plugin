---
name: ulazai-images
description: Maak met UlazAI private AI-afbeeldingen (hero's, thumbnails, mockups, assets) voor een project. Gebruik deze skill wanneer iemand een afbeelding wil laten genereren of modellen wil vergelijken.
---

# Afbeeldingen maken met UlazAI

Gebruik de UlazAI-tools in deze volgorde:

1. `get_ulazai_account` — controleer of het account gekoppeld is en hoeveel allowance er nog is. Vraag niet om betaalgegevens; verwijs bij een lege allowance naar https://ulazai.com/pricing/.
2. `search_ulazai_models` — kies een model dat past bij de vraag (fotorealistisch, illustratie, snel/goedkoop). Noem kort waarom.
3. `prepare_ulazai_image` — leg prompt, formaat en model vast en toon de samenvatting aan de gebruiker.
4. `create_ulazai_image` — genereer pas na een expliciet akkoord; dit verbruikt allowance.
5. `get_ulazai_generation` — haal het resultaat op en geef de bestands-URL door. Sla het bestand op waar de gebruiker het wil hebben (bijvoorbeeld `public/images/` of `wp-content/uploads/`).

## Regels
- Eén beeld per aanroep. Geen batches zonder overleg.
- Schrijf prompts in het Engels, concreet: onderwerp, stijl, licht, compositie, wat er níet in mag.
- Voor webgebruik: vraag om het gewenste formaat (bijvoorbeeld 16:9 voor hero's) en bewaar het bestand met een beschrijvende naam.
- Herhaal een generatie niet stilzwijgend bij een fout; meld de foutmelding en vraag hoe verder.
- Genereer geen beelden van echte personen zonder toestemming en geen merklogo's van derden.
