---
title: 'Home-Assistant config'
disqus: hackmd
---

Home-Assistant
===
![downloads](https://img.shields.io/github/downloads/atom/atom/total.svg)
![build](https://img.shields.io/appveyor/ci/:user/:repo.svg)
![chat](https://img.shields.io/discord/:serverId.svg)

## Inhoud

[TOC]

## Changelog
### 2020-04-17
Gordijnen gaan automatisch open en dicht op beweging. 

## Home-assistant documentatie

De standaard engelstalige documentatie over home-assistant staat hier. Deze pagina gaat specifiek over mijn huis en is bedoeld om vragen van gebruikers te beantwoorden, en zodat ik niet alles zelf hoef te onthouden.


Project Timeline
---
```mermaid
gantt
    %% http://mermaid-js.github.io/mermaid/#/gantt?id=a-note-to-users
    title Timeline

    section Security
    Portiek slot       :s1, 2020-05-01, 30d
    Deur sensoren        :s2, after s1, 20d
    
    section Automation
    Weer sensoren      :c1, after s2, 30d
    
    section Sensor
    Climate            : done, c1, 2020-04-01, 7d 
    Motion sensoren    :active, l1, after c1, 10d
    
    section Balkon
    LED verlichting    :b1, 2020-07-01, 10d
```

> Read more about mermaid here: http://mermaid-js.github.io/mermaid/

```mermaid
graph LR
    A[Hard edge] -->|Link text| B(Round edge)
    B --> C{Decision}
    C -->|One| D[Result one]
    C -->|Two| E[Result two]
```

User story
---

```gherkin=
Feature: Verlichting
  Als een bewoner
  Wil ik dat de lampen aan staan wanneer het donker is
  Omdat de lichtknoppen niet in dezelfde ruimte zijn. 

  Scenario: Bewoner loopt in de keuken
    Given Er zijn mensen thuis
    When Ik in de keuken loop
    And Het is donker
    And De lamp staat uit
    Then Zet de lamp aan
    And Reset de timer die de lamp uit zet
```

## Automations
### Woonkamer
#### Gordijnen
De gordijnen gaan open bij beweging in de woonkamer, na zonsopkomst. 
De gordijnen gaan dicht bij beweging, 30 minuten na zonsondergang. 

## Appendix and FAQ

:::info
**Find this document incomplete?** Leave a comment!
:::

###### tags: `Documentation`
