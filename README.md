# Teste para vaga de Estágio em Analista de Qualidade - Desenvolvido pela empresa MAGAZORD

Este repositório apresenta a elaboração do teste desenvolvido pela candidata Maria Eduarda Ruck durante o processo seletivo referente à vaga de Estágio em Analista de Qualidade disponibilizado pela empresa Magazord.

>## O teste é separado nas seguintes etapas: 
**1.** Criar casos de teste para validar a entrada de dados nos campos modificados apresentados pelo cadastro de usuários. O cadastro possui os seguintes campos:
- Nome completo
- E-mail
- Número de telefone
- Data de nascimento
- Endereço (com campos para rua, cidade, estado e CEP)

  Houve alterações nos campos mencionados acima no cadastro do cliente, segue abaixo testes que podem ser realizados para averiguar as informações citadas evitando possíveis erros.
  
### **Resultado** 
  Após serem feitas alterações no sistema de gerenciamento de cadastros mencionado acima, é necessário realizar uma série de testes para verificar se o sistema está em funcionamento pleno. Sendo assim, é importante validar cada campo inserindo dados em formatos diversos, seguindo situações hipotéticas, a fim de confirmar o sucesso do cadastramento.
  Alguns testes que poderiam ser realizados, por exemplo, seriam
- No campo do nome, é possível inserir caracteres especiais como acentuação? E quanto à pontuação? Há um campo mínimo de caracter a ser preenchido? E se, por exemplo, o usuário digitar somente o seu primeiro nome, esquecendo, assim, de inserir seu último nome? Será aceito o cadastro dessa pessoa? E se o usuário introduzir números? Como evitar tais possíveis erros? 
- No e-mail, além de ser necessário realizar a formatação do texto a ser inserido pelo usuário (como o uso do caracter especial '@' e a finalização '.com', por exemplo) seria interessante realizar testes com e-mails existentes e não existentes e, também, inserir um e-mail já cadastrado anteriormente. O sistema irá permitir um e-mail duplicado? Como evitar essa situação?
- A mesma lógica deve ser aplicada em todos os campos do cadastro. Na seção do número de telefone, seria interessante inserir um número válido e, claro, um número inválido, além de verificar também se o sistema está aceitando os dados dentro da formatação correta do país. Nesse caso, pode ser exigido um número de espaçamento mínimo e/ou máximo na hora de inserir os dados. Sabemos que o prefixo no Brasil seria +55, mais o código do DDD referente ao Estado do usuário e, por fim, seu número de telefone. Essas informações devem ser levadas em consideração na fase de desenvolvimento do sistema a fim de evitar a coleta de dados incompletos ou inválidos.
- No campo da data de nascimento, qual vai ser o formato aceito? Há alguma idade mínima? E se, por um acaso, o usuário errar o ano, excedendo a sua idade para além dos 100 anos de vida? Esses dados deverão ser validados em tempo real durante o preenchimento do cadastro.
- O mesmo valeria para o campo do CEP. E se, por exemplo, não for inserido um CEP completo ou existente? O sistema irá verificar e retornar um feedback ao usuário em tempo real? Seria importante realizar esses testes.
- Já no campo do CPF, onde obrigatoriamente devem ser inseridos 11 dígitos, seria necessário realizar testes nesse campo inserindo CPFs válidos e inválidos, verificando se o sistema os aceita ou não, além de conferir se o mesmo aceita números inferiores a 11 dígitos.

  A **obrigatoriedade do preenchimento** e o **feedback** ao usuário seria uma regra geral que se encaixa em todos os campos a serem preenchidos durante o cadastro do usuário, além de, claro, a validação em tempo real dos dados inseridos.
  
  É importante, também, visualizar o layout do _site_ através da lente do usuário e realizar alguns questionamentos. Os campos obrigatórios mencionados acima estão destacados de forma clara? Está evidente que estes campos precisam ser preenchidos? Os elementos visuais servem de auxílio para o usuário, ou o distraem? Os botões estão localizados de forma correta? O espaçamento, as cores do layout e o tamanho das letras podem ser mudados para aprimorar a experiência do usuário? Quais possíveis erros essas alterações evitariam? O _site_ foi projetado de forma tal onde o "passo a passo" a ser seguido pelo cliente seja, de fato, intuitivo?
  
  Esses questionamentos devem ser levados para à equipe de front-end, a fim de buscar melhorias e evitar possíveis erros na hora do preenchimento do cadastro. Por exemplo, caso o usuário esquecer de preencher um campo corretamente, pode ser feita uma validação dos dados pelo lado do cliente (em sua tela de computador ou celular, como por exemplo pela aparição de um aviso) para garantir que esses dados sejam preenchidos conforme os critérios do sistema, antes mesmo do cadastro ser enviado para o servidor.
  
  Ainda, essa mesma validação deve ser feita pelo lado de quem desenvolveu o código do sistema. Podem ser usadas expressões regulares para que o usuário insira os dados dentro do formato exigido, como, por exemplo, o número de telefone (que não deve aceitar strings como letras), e a data de nascimento (que pode ser codificada para aceitar somente números). O mesmo se aplica para o campo do CPF, o código foi desenvolvido de forma tal pra aceitar a inserção de pontuação? E o campo do e-mail? O usuário está ciente dessa configuração? Como transmitir de forma clara o que está sendo solicitado para o usuário? 
  
  Erros na hora do preenchimento do cadastro (como inserir letras onde deveria haver números, ou a inserção de um endereço incorreto, e-mail, e por aí vai) podem ser evitados antes mesmo do envio desse cadastro. Há diversas validações que podem ser feitas enquanto o usuário preenche o seu cadastro. Esses eventuais erros de digitação podem e devem ser considerados durante o desenvolvimento do sistema pela equipe do back-end, ao introduzir na construção do código bibliotecas e condicionais, como as estruturas if e else, ou for e while,  onde é criado condições necessárias para o preenchimento dos campos presentes no cadastro. Além disso, podem ser colocadas linhas de código que irão automaticamente verificar o formato do campo inserido, desde o tipo (int, string, float etc.) até o tamanho (quantidade de caracteres), e ainda, é possível fazer uma conversão automática, além de desconsiderar os caracteres especiais que o usuário digitar, desconsiderar strings específicas como letras ou números nos campos inadequados para tal, entre outros.
  
  É muito mais difícil e custoso contornar dados nulos, incorretos ou enviesados após a coleta dos mesmos. Para evitar que seja feito esse tipo de tratamento de dados (eliminação de dados nulos, repetidos ou incoerentes) e, também, para evitar a perda deles, é importante realizar uma série de procedimentos para garantir o sucesso da coleta desses dados (na hora de realizar o cadastro do usuário) e, claro, testá-los. Raramente o analista conseguirá resgatar um dado que não foi entregue da forma correta, logo, a importância de realizar testes do serviço que está sendo prestado (e esperado) é essencial.

  Em resumo, os testes a serem realizados seriam:
1. Avaliar a experiência do usuário durante a usabilidade do sistema, certificando que o mesmo seja de fácil compreensão, intuitivo e informativo;
2. Tornar ciente ao usuário a obrigatoriedade do preenchimento dos campos mencionados, dando feedback para ele em cada interação;
3. Considerar, durante a construção do código, possíveis erros de digitação e/ou desatenção pela parte do usuário, colocando limitações e conversões (através de condicionais, expressões, bibliotecas, loops etc.) que evitarão a inserção de dados corrompidos/inconsistentes e o fracasso do cadastramento;
4. Validar em tempo real os dados inseridos antes dos mesmos serem entregues ao servidor (confirmar o CEP, o CPF, etc.);
5. Testar a compatibilidade em diversos desktops, navegadores, mobiles etc.;
6. Certificar que o sistema esteja em perfeito estado de funcionamento, validando os dados inseridos e armazenando-os com segurança, tendo em vista a política de privacidade e a ética do usuário; 
7. Testar a exibição dos dados inseridos;
8. Conferir a performance do sistema, certificando que o mesmo funcione com diversos acessos simultâneos;
   
  Nesse sentido, é importante também averiguar a medição da velocidade, da capacidade de processamento, a estabilidade do serviço (do sistema em questão), da segurança dos dados que estão sendo coletados (se estão sendo armazenados de forma correta e ética), e da capacidade do sistema (levando em consideração um número grande de acessos/demanda).

  E, claro, **testar a usabilidade** do sistema ao longo de todo o percurso percorrido. Manter um monitoramento constante, aceitar críticas e sugestões dos usuários, visando sempre a qualidade do serviço que está sendo prestado e a experiência do cliente que está usufruindo do mesmo.
  
**2.** O cliente enviou o seguinte erro causado pela tentativa de importação de um arquivo XML de GNRE no site <https://www.gnre.pe.gov.br:444/gnre/v/lote/processar>. Analise o XML exportado e documente o motivo pelo qual o erro está acontecendo.

```
<?xml version="1.0" encoding="UTF-8"?>
<TLote_GNRE xmlns="http://www.gnre.pe.gov.br" versao="2.00">
    <guias>
        <TDadosGNRE versao="2.00">
            <ufFavorecida>SE</ufFavorecida>
            <tipoGnre>0</tipoGnre>
            <contribuinteEmitente>
                <identificacao>
                    <CNPJ>17637*********</CNPJ>
                </identificacao>
                <razaoSocial>Teste Ltda</razaoSocial>
                <endereco>Rua Emilio Paulo Pilz</endereco>
                <municipio>15802</municipio>
                <uf>SC</uf>
                <cep>89280831</cep>
            </contribuinteEmitente>
            <itensGNRE>
                <item>
                    <receita>100102</receita>
                    <documentoOrigem tipo="10">581</documentoOrigem>
                    <referencia>
                        <mes>05</mes>
                        <ano>2023</ano>
                    </referencia>
                    <dataVencimento>2024-01-11</dataVencimento>
                    <valor tipo="11">491.80</valor>
                    <contribuinteDestinatario>
                        <identificacao>
                            <CNPJ>05578765000127</CNPJ>
                        </identificacao>
                        <razaoSocial>QUALITY BRINDES LTDA</razaoSocial>
                        <municipio>00308</municipio>
                    </contribuinteDestinatario>
                    <camposExtras>
                        <campoExtra>
                            <codigo>77</codigo>
                            <valor>42230517637*********55005000000**1000015949</valor>
                        </campoExtra>
                    </camposExtras>
                </item>
            </itensGNRE>
            <valorGNRE>491.80</valorGNRE>
            <dataPagamento>2024-01-11</dataPagamento>
        </TDadosGNRE>
    </guias>
</TLote_GNRE>
```
### **Resultado**
  Ao analisar a mensagem de erro informada e o arquivo exportado, é possível encontrar uma incongruência nas informações inseridas durante a construção do código. Mais especificamente, o erro se encontra na linha,
  
                      <referencia>
                        <mes>05</mes>
                        <ano>2023</ano>
                    </referencia>
                    <dataVencimento>2024-01-11</dataVencimento>
                    
  Parece que o sistema da GNRE espera que a data de referência seja equivalente à data de validade, no caso, o correto seria,
  
                        <referencia>
                        <mes>01</mes>
                        <ano>2024</ano>
                    </referencia>
                    <dataVencimento>2024-01-11</dataVencimento>

  Porém, é válido verificar através do _site_ ou até mesmo entrando em contato com o **suporte técnico** para averiguar se são essas realmente as alterações necessárias a serem feitas. É importante consultar o tipo de formato de texto que é aceito pelo _site_ do GNRE, assim como as regras a serem seguidas e as informações a serem inseridas.

  Esse erro específico deve ser repassado para à equipe do suporte ao cliente, para que possam ser feitas as alterações necessárias (dentro dos requisitos do código de arquivo XML e do GNRE), além de ser realizado um novo teste de importação, para enfim levar a solução até o cliente.
