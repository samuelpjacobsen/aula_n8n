# Configuração Proposta comercial N8N

## Para utilizar o copia e cola, é necessário ativar a opção Expression em cada campo
<img width="305" alt="image" src="https://github.com/user-attachments/assets/99e266f9-7dbd-4772-b298-8bed28fd9349">



## On form Submission
```
Empresa
```
```
Tema
```
```
Data
```
```
Subtitulo
```
```
Contexto
```
## Edit fields

- **Name**:
  ```
  chatInput
  ```
- **Value**: 
  ```
  Tema: {{ $json.Tema }}, Subtítulo: {{ $json.Subtitulo }}, Contexto: {{ $json.Contexto }}
  ```

## AI Agent

**System prompt**:
 ```
Você é um especialista em criar apresentações empresariais. Com base no tema, subtítulo e contexto fornecidos, crie um texto inovador e envolvente que reflita o contexto de forma clara e objetiva. O texto não deve conter menções diretas ao tema ou subtítulo. Retorne apenas o conteúdo relacionado ao contexto.

{{ $json.chatInput }}
 ```
# Google Docs

### Empresa

Old Text
 ```
{empresa}
 ```
New Text
 ```
{{ $('On form submission').item.json.Empresa }}
 ```

### Tema

Old Text 
 ```
{tema}
 ```
New Text 
 ```
{{ $('On form submission').item.json.Tema }}
 ```

### Data

Old Text
 ```
{data}
 ```
New Text
 ```
{{ $('On form submission').item.json.Data }}
 ```

### Subtitulo

Old Text
 ```
{subtitulo}
 ```
New Text
 ```
{{ $('On form submission').item.json.Subtitulo }}
 ```

### Contexto

Old Text
 ```
{contexto}
 ```
New Text
 ```
{{ $json.output }}
 ```
