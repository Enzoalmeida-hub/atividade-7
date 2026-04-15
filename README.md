# atividade-7
algoritmo "validadorPIX"
var
   valor_pix, saldo_atual, limite_cheque: real

   inicio
      // 1. Solicita o valor da transferência e o saldo
         escreva("Digite o valor do Pix: R$ ")
            leia(valor_pix)
               escreva("Digite seu saldo atual: R$ ")
                  leia(saldo_atual)

                     // 2. Verifica se o saldo é suficiente
                        se (saldo_atual >= valor_pix) entao
                              escreval("Transação realizada")
                                 senao
                                       // 3. Caso não tenha saldo, solicita o cheque especial
                                             escreval("Saldo insuficiente na conta corrente.")
                                                   escreva("Digite o seu limite de cheque especial: R$ ")
                                                         leia(limite_cheque)

                                                               // 4. Verifica se o saldo + cheque especial cobrem o valor
                                                                     se (saldo_atual + limite_cheque >= valor_pix) entao
                                                                              escreval("Transação via Cheque Especial")
                                                                                    senao
                                                                                             escreval("Saldo Insuficiente")
                                                                                                   fimse
                                                                                                      fimse

                                                                                                      fimalgoritmo
                                                                                                      