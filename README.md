# APIDRIBL #

I am trying to document the public API of dribl.com

the swagger is presented here: https://data-monkey.github.io/apidribl/#/


the dribl app has many concepts that need to be related to each other. 


```mermaid
erDiagram
    Club ||--o{ Team : has
    Ground ||--o{ Field : has
    Tenant ||--o{ Field : owns
    Tenant ||--o{ Club  : assosiation_of
    Team }|..|{ Field : plays_on
    Competition ||--o{ League : has
    League }|..|{ Team : has
    League ||--o{ Ladder : has
    Fixture ||--o{ Match : has
    Fixture ||--o{ Field : plays_on
    Ladder ||--o{ Ladder_Entry : has
    Ladder_Entry ||--o{ Match : has_recent
    Season  ||--o{ Competition   : has
    League ||--o{ Round   : has
    Club ||--|| Ground : home_ground
    Round ||--o{ Fixture : has
```


I am still working out the relationships ...
