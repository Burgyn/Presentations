1. Ukázať klasický Release
   - Vyklikať si jednu službu
   - Ukázať GATE
2. Spraviť kostru releasu
   - použi snippet
   - Vysvetliť stages
   - Vysvetliť deploy job
   - Deploy
   - Ukázať environmenty
   - Aprovals
3. Nasadiť jednu službu
   - Deploy task zo snippetu
   - Pridať zdoj pipeline
   - Premenné
     - Čo s nastaveniami služby? Štandardne connection string. Secret nie v source kontrole.
     - V YAML, v TEMPLATE, v PIPELINE, v LIBRARY
     - Pridaj ConnectionStrings.DefaultConnection premennú
     - Použi Transform task
     - Download artifacts
4. Nasadenie vššetkých služieb
   - použiť template (microservices)
   - použiť variables z template
   - ukázať odkaz na Variable group
   - ukázať použitie powershellu
5. Nasadenie API Gateway
   - Template
   - Vysvetli apigateway, ukáž powershell
   - Spusti nasadenie
   - Zatiaľ ďalej ukazuj zvyšok
6. Nasadenie klienta
   - Pridaj nový pipeline resource
   - Pridaj download artifacts (všade)
   - použi template - ďalší agent kvôli paralelizácií
7. Ostatné veci ukáž na plnej template
   - nasadenie do testu
     - vytvorenie prostrednia
     - nasadiť
     - spustiť testy
     - zmazať prostredie
   - nasadenie staging
   - swap produkcia


Čo chceme a ešte nemáme
- PR spustiť integračné a UI testy
- asynchrónne nasadenie služieb v rámci jedného jobu
- detekcia, ktoré služby boli zmazané a len tie nasadiť