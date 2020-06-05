---?image=ApiGatewayOcelot/assets/img/slide.png

---

## Agenda

- Aký problém riešime?
- Čo je to Api Gateway pattern?
- Ocelot
- Demo
- Q&A

---

@img[span-75](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/media/direct-client-to-microservice-communication.png)

Note:
Mikroslužby sú aktuálny trend. Riešia veľa problémov, ktoré sme mali s monolymi, ale taktiež veľa problémov, alebo skôr otázok prinášajú.
(Tranzakcie, duplicita dát, managovanie všetkých služieb, ...)
Jednou z otázok je aj ako má klient pristupovať k jednotlivým službám. Pokiaľ sa jedná o pár služiem tak ešte ok. Ale ak sa jedná o naozaj väčší problém tak už to je celkom zložitejšie.

---

## Otázky

- Ako minimalizovať počet dotazov na server?
- Ako redukovať komplexnosť klienta?
- Ako spravovať prierezovú funkčnosť?
- Ako pripraviť API pre viaceré typy klientov?
- ...

Note:
*(množstvo adries, zbytočná business logika, previazanie s konkrétnymi službami, ...)*
*(Autorizácia, logovanie, kešovanie, ...)*
*(browser, mobile, ...)*

---

@img[span-75](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/media/direct-client-to-microservice-communication-versus-the-api-gateway-pattern/custom-service-api-gateway.png)

---

@img[span-75](https://docs.microsoft.com/en-us/dotnet/architecture/microservices/architect-microservice-container-applications/media/direct-client-to-microservice-communication-versus-the-api-gateway-pattern/multiple-custom-api-gateways.png)

---

## Vlastnosti

@snap[text-06]

- Reverse proxy / gateway routing
- Request aggregation
- Cross-cutting concerns / gateway offloading
  - Authentication and authorization
  - Service discovery integration
  - Response caching
  - Retry policies, circuit breaker, and QoS
  - Rate limiting and throttling
  - Load balancing
  - Logging, tracing, correlation
  - Headers, query strings, and claims transformation
  - IP whitelisting
@snapend

---

## Možnosti

- Azure
  - API Management
  - *Aplication Gateway*
  - *Front Door*
- Ocelot
- ...

---

## Ocelot
<!-- PrepnuŤ sa na Ocelot. Upozorni na to, že nevie swagger -->
---

## DEMO

---

@img[span-75](ApiGatewayOcelot/assets/img/schema-base.png)

---

@img[span-75](ApiGatewayOcelot/assets/img/schema-withoutOcelot.png)

---

@img[span-75](ApiGatewayOcelot/assets/img/schema-full.png)

---

Ako to používame my.
@img[span-75](ApiGatewayOcelot/assets/img/full-schema.png)

---?image=ApiGatewayOcelot/assets/img/final.png
