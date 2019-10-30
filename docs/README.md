# Guião para fazer tabelas de resumos de avaliação

## Visão Geral

A tabela guarda a percentagem de uma avaliação organizada por cadeira e por componente que pode ser **Exame**, **Teste**, **Projeto**, **Teorico-Pratica** e **Observações**

## Como fazer
### No início de todos os html, não tocar nisto
(Pode-se tocar apenas na parte onde vem o ano, o semestre e intervalo do ano letivo)
```html
<!DOCTYPE html>
<html>
<head>

<meta charset="UTF-8">
<meta name="viewport" content="width=737px, initial-scale=1">
<link rel="stylesheet" type="text/css" href="../../css/styles.css">

</head>
<body>
<center>
	<h1>Avaliação Xº semestre (Yº ano)</h1>
	<h3>De <em>DD/MM</em> a <em>DD/MM</em></h3>
</center>
<table>
  <tr>
    <th></th>
    <th>Exame</th>
    <th>Testes</th>
    <th>Projeto</th>
    <th>Teórico-práticas</th>
    <th>Observações</th>
  </tr>
```
### **Só** podes alterar a partir daí (da primeira ocurrência de `</tr>` para baixo)

A partir daí cada linha é formada por isto

```html
<tr>
    <th>Nome da Cadeira</th>
    <td>
        <div>Percentagem_Exame%
            <span class="text-2-line">
                <b>1ª:</b> DD/MM H24hMin X.Y.Z <br> 
                <b>2ª:</b> DD/MM H24hMin X.Y.Z
            </span>
        </div>  
    </td>
    <td>
        <div>Percentagem_Teste%
            <span class="text-2-line">
                <b>1º:</b> DD/MM <br> 
                <b>2º:</b> DD/MM
            </span>
        </div>  
    </td>
    <td>
        <div>Percentagem_Projeto%
            <span class="text-1-line">
                <b>X</b>
            </span>
        </div>  
    </td>
    <td>
        <div>Percentagem_TP%
            <span class="text-1-line">
                <b>Libsum</b>
            </span>
        </div>  
    </td>
    <td>
        <div>Percentagem_Observações%
            <span class="text-1-line">
                <b>Libsum</b>
            </span>
        </div>  
    </td>
</tr>
```
Portanto, basta repetir isto até ao final e ir alterando pelos valores e textos corretos

## O que fazer quando o texto que quero meter numa célula da tabela não cabe todo?

**Solução**: Na célula da tabela colocar o mais importante do que queres dizer e no final colocar `<sup>[1]</sup>`. E, no final do *body*, explicar essa referência que acabaste de fazer.
