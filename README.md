# Biblioteca para Rastreio de Objetos dos Correios

Através desta biblioteca você será capaz de recuperar o status, data, origem e destino do objeto com resposta via JSON.

<br>

# Instalando
```shell
npm i rastreamento-correios
```
ou
```shell
yarn add rastreamento-correios
```

<br>

# Rastreando um objeto
```js
const correios = require('rastreamento-correios')
 
correios.sro.rastrearObjeto('QF123456789BR').then(function(res){
    console.log(res)
})
```

<br>

# Exemplo de resposta
```json
{
  "rastreio": [
    {
      "status": "Status: Objeto em trânsito - por favor aguarde", 
      "data": "Data: 29/06/2021 | Hora: 11:35",
      "origem": "Origem: Agência dos Correios - Sao Paulo / SP",  
      "destino": "Destino: Unidade de Tratamento - Cajamar / SP"  
    },
    {
      "status": "Status: Objeto em trânsito - por favor aguarde", 
      "data": "Data: 29/06/2021 | Hora: 19:02",
      "origem": "Origem: Unidade de Tratamento - Cajamar / SP",   
      "destino": "Destino: Unidade de Tratamento - Fortaleza / CE"
    },
    {
      "status": "Status: Objeto em trânsito - por favor aguarde",
      "data": "Data: 03/07/2021 | Hora: 16:55",
      "origem": "Origem: Unidade Operacional - Fortaleza / CE",
      "destino": "Destino: Agência dos Correios - Frecheirinha / CE"
    },
    {
      "status": "Status: Objeto em trânsito - por favor aguarde",
      "data": "Data: 03/07/2021 | Hora: 16:55",
      "origem": "Origem: Unidade Operacional - Fortaleza / CE",
      "destino": "Destino: Agência dos Correios - Frecheirinha / CE"
    }
  ],
  "status_code": 200
}
```