# idas

IDAS ist eine von ADDIX entwickelte Lösung zur dynamischen E-Mail-Alarmierung bei Grenzwertüberschreitungen

IDAS reagiert bei definierten Grenzwertüberschreitungen von NGSI-Entitäten und arbeitet die hinterlegten Alarmketten automatisch ab um gezielte Benachrichtigungen an relevante Empfänger verteilt.

### Einsatz im Projekt

#### ⚠️ Alarmierung bei Grenzwertüberschreitungen

IDAS überwacht NGSI-Alarm-Entitäten. Sobald ein Alarm im MLA erstellt wurde wird automatisch eine Alarm-Mail generiert. Dies ermöglicht eine schnelle Reaktion auf veränderte Zustände in Echtzeit.

#### 📧 Gezielte Verteilung von Alarmen

Die Alarme werden in Alarmketten organisiert, die spezifische Empfängergruppen erreichen. Durch die präzise Verteilung der Benachrichtigungen wird gewährleistet, dass die richtigen Personen zur richtigen Zeit informiert werden, um zeitnah auf potenziell kritische Situationen zu reagieren.

Mit IDAS erhalten Organisationen eine zuverlässige Lösung zur Überwachung von Grenzwerten und zur effizienten Verteilung von Alarmen, wodurch eine proaktive Reaktionsfähigkeit bei Abweichungen von definierten Parametern gewährleistet wird.

## Voraussetzungen

* Kubernetes 1.23+
* Helm 3.8.0+

## Installing the chart

Check out this repository and install the chart

```bash
$ cd idas
$ helm install <my-release> helm --values <values file> -n <namespace>
```

alternativ:

```bash
$ helm upgrade --install <my-release> helm --values <values file> -n <namespace>
```

Beispiel:

```bash
$ helm upgrade --install my-release helm -n my-namespace --create-namespace --values <values file>
```

## Parameter

| Name                    | Description                                     | Value                      |
|:------------------------|:------------------------------------------------|:---------------------------|
| env.DEBUG               |                                                 | info                       |
| env.KEYCLOAKURL         |                                                 | https://localhost          |
| env.CLIENTID            |                                                 | ""                         |
| env.CLIENTSECRET        |                                                 | ""                         |
| env.TOKENINTERVAL       |                                                 | 192100                     |
| env.ORIONURL            |                                                 | https://localhost          |
| env.NGSILDTENANT        |                                                 | mytenant                   |
| env.SMTPHOST            |                                                 | ""                         |
| env.SMTPPORT            |                                                 | 465                        |
| env.SMTPUSER            |                                                 | ""                         |
| env.SMTPPASSWORD        |                                                 | ""                         |
| env.SMTPSENDER          |                                                 | ""                         |
| env.SMTPMAILTO          |                                                 | ""                         |

## Upgrading the chart

To upgrade the chart with the release name my-release:

```bash
$ helm upgrade <my-release> helm --values <values file> -n <namespace>
```

## License

Copyright © 2024 ADDIX GmbH.

Licensed under the Apache License, Version 2.0 (the "License"); you may not use this file except in compliance with the License. You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software distributed under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.