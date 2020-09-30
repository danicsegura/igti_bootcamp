//Informe o setor entre aspas como parâmetro da função SalarioEmpresa para retornar a busca do nome do funcionário com o maior e o menor salário deste setor e a média salarial do setor. Caso nada seja informado, a busca retorna os valores para toda a empresa.
//Setores disponíveis: "Administrativo", "Comercial" e "Produção".

SalarioEmpresa();

function SalarioEmpresa(setor){
var fs = require("fs");
//importar arquivo json de funcionarios contendo nome, salario e setor
fs.readFile("funcionarios.json", "utf-8", function(err, data){
            if (err){
                console.log(err);
            } else {
                var json = JSON.parse(data);
                var maiorSalario = 0;
                var menorSalario = 9000;
                var funcMaiorSalario = "";
                var funcMenorSalario = "";
                var somaSalario = 0;
                var mediaSalario;
                var quantSetor = 0;
                    //iterar pela lista de funcionários
                    for (var i = 0; i < json.funcionarios.length; i++){
                        //caso setor não tenha sido informado: toda a empresa
                        if (setor === undefined){
                            somaSalario += json.funcionarios[i].salario;

                            //calculo maior salario de toda a empresa
                            if (json.funcionarios[i].salario > maiorSalario) {
                                maiorSalario = json.funcionarios[i].salario;
                                funcMaiorSalario = json.funcionarios[i].nome;
                
                            //calculo menor salario de toda a empresa
                            } else if (json.funcionarios[i].salario < menorSalario){
                                menorSalario = json.funcionarios[i].salario;
                                funcMenorSalario = json.funcionarios[i].nome;
                            }
                        //caso setor tenha sido informado
                        } else{
                            if (json.funcionarios[i].setor == setor){
                                quantSetor++;
                                somaSalario += json.funcionarios[i].salario;
                                //calculo maior salario do setor informado
                                if (json.funcionarios[i].salario > maiorSalario) {
                                    maiorSalario = json.funcionarios[i].salario;
                                    funcMaiorSalario = json.funcionarios[i].nome;
                    
                                //calculo menor salario do setor informado
                                } else if (json.funcionarios[i].salario < menorSalario){
                                    menorSalario = json.funcionarios[i].salario;
                                    funcMenorSalario = json.funcionarios[i].nome;
                    
                                }
                            }
                        }
                        //calculo media salarial toda a empresa ou setor informado
                        if (setor === undefined){
                            mediaSalario = somaSalario / json.funcionarios.length;
                        } else {
                            mediaSalario = somaSalario / quantSetor;
                    }
                }
            }
        //retorna resultados
        console.log("O maior salário deste setor é: "+maiorSalario);
        console.log("O funcionário com o maior salário do setor é: "+funcMaiorSalario);
        console.log("O menor salário deste setor é: "+menorSalario);
        console.log("O funcionário com o menor salário do setor é: "+funcMenorSalario);
        console.log("A soma total de todos os salários dste setor é: "+somaSalario);
        console.log("A media salarial deste setor é: "+mediaSalario);
    })
}
