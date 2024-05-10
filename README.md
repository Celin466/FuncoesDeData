# FuncoesDeData
1- Função para comparar datas<br/>
<br/>
function compararData(data1, data2) {<br/>
    if (data1.getTime() > data2.getTime()) {<br/>
        return data1;<br/>
    }<br/>
    return data2;<br/>
}<br/>
<br/>
Ela recebe dos inputs da tela as datas e faz a comparação  pegando o tempo das datas e comparando se a primeira é maior que a segunda, se for retorna a primeira, se não, automaticamente
  retorna a segunda.<br/>
<br/>
  2- Função para calcular o intervalo entre as datas sendo que a primeira data obrigatoramente vai ser a maior.<br/>
  function intervaloData(data1, data2) {<br/>
    if (data1.getTime() >= data2.getTime()) {<br/>
        alert("Primeira data deve ser mais antiga!");<br/>
        return false;<br/>
    }<br/>
    return (data2.getTime() - data1.getTime()) / 1000;<br/>
}<br/>
<br/>
A função recebe os parâmetros vindos dos inputs da tela, e faz a comparação utilizando o getTime nas variaveis do tipo data de data1 e data2, ele vai pegar a data por completo, e retornar os milesegundos de  1 de Janeiro de 1970 00:00:00 até a data atual, faz a validação para verificar se a primeira é maior, se não retorna a data em segundos para o alert que está chamando.<br/>
<br/>
3- Função que retorna a data atual no formato: hora:minuto - dia/mês/ano.<br/>
function converterData(dataAtual) {<br/>
    let ano = (dataAtual.getFullYear()).toString();<br/>
    let mes = (dataAtual.getMonth() + 1).toString();<br/>
    let dia = (dataAtual.getDate()).toString();<br/>
    let horas = (dataAtual.getHours()).toString();<br/>
    let minutos = (dataAtual.getMinutes()).toString();<br/>
    if (mes.length < 2) {<br/>
        mes = "0" + mes;<br/>
    }<br/>
    if (dia.length < 2) {<br/>
        dia = "0" + dia;<br/>
    }<br/>
    if (horas.length < 2) {<br/>
        horas = "0" + horas;<br/>
    }<br/>
    if (minutos.length < 2) {<br/>
        minutos = "0" + minutos;<br/>
    }<br/>
<br/>
    let novaData = `${horas}:${minutos} - ${dia}/${mes}/${ano}`;<br/>
    return novaData;<br/>
}<br/>

A função recebe a dataAtual que é um objeto Date(), com a data atual, faz a separação dos elementos, hora minuto etc... ,  faz várias verificações para validar se os campos tem a quantidade certa de caracteres, no caso dois por variavel, caso não tenha é adicionado um zero, assim retornando a novaData no padrão string como solicitado.




