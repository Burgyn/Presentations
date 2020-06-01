---

## Building .NET Core API Gateway with Ocelot & MMLib.SwaggerForOcelo

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

@img[span-75](/assets/img/schema-base.png)

---

@img[span-75](/assets/img/schema-withoutOcelot.png)

---

@img[span-75](/assets/img/schema-full.png)

---

Ako to používame my.
- Autorizácia
- transformácia query stringov na claims

---?color=linear-gradient(100deg, white 50%, #1F6ED4 50.2%)

@snap[west span-60]
@img[shadow](https://scontent-frx5-1.xx.fbcdn.net/v/t1.0-9/71581737_10156577632582844_3229986981945540608_o.jpg?_nc_cat=110&_nc_oc=AQmfuBqruWK48h2YiDZo1nCh1_ipiao0dEZ_wBgBI0bXYSw5Vxj40Zqmhy37ZiSu8cY&_nc_ht=scontent-frx5-1.xx&oh=b9cdb19f29b53387eb2bb51aef805016&oe=5E4712BF)
@snapend

@snap[east span-50 h3-white]
### Continuous
### integration
### / delivery
@snapend

@snap[south-east]
28.1.2020 17:00
Kros 3. poschodie
@snapend