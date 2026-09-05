# Richards agent – beslutsystem

Ett personligt beslutsystem inspirerat av Reid Hoffmans artikel
["Decision Machines"](https://www.linkedin.com/pulse/decision-machines-reid-hoffman-orrtc):
agenter jobbar autonomt och kommer tillbaka med en kort hög väl inramade
JA/NEJ-beslut i stället för statusrapporter. Richards omdöme är den knappa
resursen – systemet skyddar det.

## Delar

| Del | Var |
|---|---|
| Drive-mapp | `Lundgrens Master / 1. Pågående projekt / x - Richards agent` |
| Dashboard | Google-dokumentet `00 Dashboard – Richards agent` |
| Instruktioner | Google-dokumentet `01 Läs mig – Så fungerar systemet` |
| Daglig rutin | Claude-rutinen `Richards agent – morgonbrief` (vardagar 06:00 svensk tid) |
| Agentprompt | [`morgonbrief-prompt.md`](morgonbrief-prompt.md) i den här mappen |

## Flöde

1. Vardagsmorgnar kör rutinen agentprompten.
2. Agenten läser dashboarden (mål + gårdagens JA/NEJ-svar), följer upp svaren
   (t.ex. mejlutkast i Gmail – skickar aldrig själv), samlar underlag från
   Gmail, Google Kalender och projektmappen.
3. Den skriver `Brief ÅÅÅÅ-MM-DD` i Drive-mappen och uppdaterar dashboarden:
   projektläge, måluppföljning och max 5 nya beslutspunkter formulerade som
   JA/NEJ med alternativ, rekommendation och konsekvens.
4. Richard svarar JA eller NEJ direkt i dashboardens sektion 3. Nästa körning
   agerar på svaren och arkiverar dem i sektion 4.

## Ändringar

- Mål: redigera dashboardens sektion 1.
- Tid/frekvens/beteende: be Claude uppdatera rutinen `Richards agent – morgonbrief`
  (id `trig_019chCJjUS98vCwaNJCNc7F7`). Prompten i `morgonbrief-prompt.md` är
  källan – uppdatera den här och i rutinen samtidigt.

Drive-id:n: mapp `1pplZedVsS6YBeAONs16T8hceTthtbQEy`,
dashboard `1Osk4mkWKboHEeicg845GABsNa2QIBVWyK1NxX6Rl9TM`,
projektmapp `0B0iqfM0_AWX1TzNkb3VJdkl2Rm8`.
