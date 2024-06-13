# APIDRIBL #

I am trying to document the public API of dribl.com

the swagger is presented here: https://data-monkey.github.io/apidribl/#/


the dribl app has many concepts that need to be related to each other. 


```mermaid
erDiagram
    Club ||--o{ Team : has
    Ground ||--o{ Field : has
    Tenant ||--o{ Field : owns
    Team }|..|{ Field : plays_on
    Competition
    Season
    League
    Fixture
    Ladder
```


I am still working out the relationships ...
