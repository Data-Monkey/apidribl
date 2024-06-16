# API DRIBL #

I am trying to document the public API of dribl.com

__mc-api.dribl.com__ seems to be the public api <br>
__api.dribl.com__ is private

I have documented whatever I found in OpenAPI notation and presetned it here: </br> </br>
<b>https://data-monkey.github.io/apidribl/</b>


The public api has many endpoints based around the needs of the public websites that dribl provides. I have mostly ignored these endpoints and focused on the data related ones<br>
Website exampeles are:
- https://mwfa.dribl.com/   Manly Warringha Football Association
- https://competitions.footballnsw.com.au/ Football NSW  


## Entities ##
Dribl uses many concepts that need to be related to each other. 


```mermaid
erDiagram
    Club ||--o{ Team : has
    Ground ||--o{ Field : has
    Tenant ||--o{ Ground : uses
    Tenant ||--o{ Club  : assosiation_of
    Team }|--|{ Field : plays_on
    Competition ||--o{ League : has
    League }|--|{ Team : has
    League ||--o{ Ladder : has
    Fixture ||--o{ Match : has
    Fixture ||--o{ Field : plays_on
    Ladder ||--o{ Ladder_Entry : has
    Ladder_Entry ||--o{ Match : has_recent
    Season  ||--|{ Competition   : has
    League ||--|{ Round   : has
    Club ||--|| Ground : home_ground
    Round ||--o{ Fixture : has
    Tenant ||--|{ Season : manages
```


I am still working out the relationships ...
