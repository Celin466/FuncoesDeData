# FuncoesDeData
1- Função para comparar datas

function compararData(data1, data2) {
    if (data1.getTime() > data2.getTime()) {
        return data1;
    }
    return data2;
}

Ela recebe dos inputs da tela as datas e faz a comparação  pegando o tempo das datas e comparando se a primeira é maior que a segunda, se for retorna a primeira, se não, automaticamente
  retorna a segunda.

  2- Função para calcular o intervalo entre as datas sendo que a primeira data obrigatoramente vai ser a maior.
  function intervaloData(data1, data2) {
    if (data1.getTime() >= data2.getTime()) {
        alert("Primeira data deve ser mais antiga!");
        return false;
    }
    return (data2.getTime() - data1.getTime()) / 1000;
}

A função recebe os parâmetros vindos dos inputs da tela, e faz a comparação utilizando o getTime nas variaveis do tipo data de data1 e data2, ele vai pegar a data por completo, e retornar os milesegundos de  1 de Janeiro de 1970 00:00:00 até a data atual, faz a validação para verificar se a primeira é maior, se não retorna a data em segundos para o alert que está chamando.

3- Função que retorna a data atual no formato: hora:minuto - dia/mês/ano.
function converterData(dataAtual) {
    let ano = (dataAtual.getFullYear()).toString();
    let mes = (dataAtual.getMonth() + 1).toString();
    let dia = (dataAtual.getDate()).toString();
    let horas = (dataAtual.getHours()).toString();
    let minutos = (dataAtual.getMinutes()).toString();
    if (mes.length < 2) {
        mes = "0" + mes;
    }
    if (dia.length < 2) {
        dia = "0" + dia;
    }
    if (horas.length < 2) {
        horas = "0" + horas;
    }
    if (minutos.length < 2) {
        minutos = "0" + minutos;
    }

    let novaData = `${horas}:${minutos} - ${dia}/${mes}/${ano}`;
    return novaData;
}

A função recebe a dataAtual que é um objeto Date(), com a data atual, faz a separação dos elementos, hora minuto etc... ,  faz várias verificações para validar se os campos tem a quantidade certa de caracteres, no caso dois por variavel, caso não tenha é adicionado um zero, assim retornando a novaData no padrão string como solicitado.




