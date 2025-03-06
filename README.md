# GG-TokenStudio-Test

sperimentazione super-basic di applicazione tokens a file library Figma e diretti "discententi" file visual con override di temi diversi.

## Requisiti

### File Json
- Il file **token.json** contiene i seguenti sets:
  - _core_
  - _light_
  - _dark_
  - _theme A_
  - _theme B_
- I set **light** e **dark** ereditano i token del set **core** 
- I set **theme A** e **theme A** contengono override di alcuni token contenuti nel set **light** 

### [Progetto Figma](https://www.figma.com/files/team/963112800667377202/project/347445247/Test-Token-Studio?fuid=707952160462890638) 
- Il Progetto Figma contiene i seguenti file:
  - 1 file **Library** [Figma Library](https://www.figma.com/design/426hJbP1fFL8LTpJ0wbvqZ/mini-TS-Library?m=auto&t=Ra2ZqL484rIK2YQ6-1)
    - contiene _Components_ globali
  - 2 file **visual** [Figma Theme A](https://www.figma.com/design/bheS5NCzBKPzBxyGrhM42a/mini-TS-Visual-Theme-A?m=auto&t=Ra2ZqL484rIK2YQ6-6) e [Figma Theme B](https://www.figma.com/design/uIZ6W2U7gr0b81rkLGZJqM/mini-TS-Visual-Theme-B?m=auto&t=Ra2ZqL484rIK2YQ6-6)
    - ereditano i _Components_ del file file library
    - alle _Instances_ sono applicati _Override_
- Tramite il plugin _Token Studio for Figma_ i components del file library sfruttano tokens definiti nei set **core** e **light** del file _token.json_
- Tramite il plugin _Token Studio for Figma_ ai file visual sono applicati rispettivamente i set **theme A** e **theme B**

## Risultato atteso
i file visual _Theme A_ e _Theme B_ mantengono il collegamento con il file library, ereditando le modifiche ai componennts (o l'introduzione di nuovi), pur differenziandosi nell'aspetto tra loro e dalla library, grazie agli override specifici aplicati dei sets _Theme A_ e _Theme B_ del file json.
