# Teste-Tecnico-QA-Tester-4blue
Teste Técnico – QA Tester - Processo Seletivo – 4blue

Bugs encontrados:

## Canário 1
Título: Tela permite cadastro de contas duplicadas.

Descrição: A tela de Criação de Conta está permitindo a criação de múltiplas contas utilizando o mesmo e-mail, sem realizar validação de duplicidade no momento do cadastro.

Passos para reproduzir: https://www.loom.com/share/20e7b703f2414287ad2f1f58002fcdb7
1.	Acessar a tela Criar conta.
2.	Preencher o formulário com um e-mail já cadastrado no sistema.
3.	Preencher os demais campos normalmente.
4.	Clicar em Criar conta.
   
Resultado atual: A tela de Criação de Conta permite a criação de uma nova conta com o mesmo e-mail, gerando registros duplicados.

Resultado esperado: A tela de Criação de Conta deve validar se o e-mail já está cadastrado e impedir a criação de contas duplicadas, exibindo uma mensagem como:  "Este e-mail já está cadastrado."

Severidade: Critica

Prioridade: Alta 

---

## Cenário 2:
Título: Validações dos inputs não está sendo realizada

Descrição: Os inputs de telefone, e-mail e senha não apresentam validações adequadas ao inserir dados inválidos. O sistema permite realizar o cadastro mesmo quando os campos estão preenchidos de forma incorreta ou fora do padrão esperado.

Passos para reproduzir: https://www.loom.com/share/01dc24fbf9e04a69bb988f4e99786f61
1.	Acessar a tela Criação de Conta.
2.	Preencher os campos telefone, e-mail ou senha com valores inválidos (ex: telefone incompleto, e-mail sem "@", senha sem caractere especial).
3.	Clicar em Criar conta.
   
Resultado atual: A tela de Criação de Conta não apresenta mensagem de erro nem bloqueia o envio do formulário, permitindo dados inválidos.

Resultado esperado: A tela de Criação de Conta deve validar os campos antes do envio, exibindo mensagens de erro quando:
•	O telefone não estiver no formato correto.
•	O e-mail não possuir formato válido.
•	A senha não atender aos requisitos mínimos (ex: 8 caracteres e 1 caractere especial).

Severidade: Alta

Prioridade: Media

---

## Cenário 3
Título: Layout da tela de Criação de Conta.

Descrição: Os inputs de Nome Completo e Telefone, assim como Senha e Confirmar Senha, não estão corretamente alinhados entre si. Os campos aparentam ter larguras diferentes e sobreposição visual, causando quebra de layout e prejudicando a padronização do formulário.

Passos para reproduzir: Ao acessar a tela de Criação de Conta já notasse os inputs fora de padrão.

Resultado atual: Os campos do formulário estão desalinhados e fora do padrão visual, causando inconsistência no layout da tela de cadastro.

Resultado esperado: Os campos do formulário de cadastro devem estar corretamente alinhados, com largura padronizada e espaçamento uniforme, respeitando o layout do container. Nenhum campo deve ultrapassar os limites do formulário ou apresentar sobreposição visual.

Severidade: Média

Prioridade: Baixa

---

## Quais 2 bugs você corrigiria primeiro e por quê? 

Os dois bugs que eu corrigiria seriam: 

Cenário 1

Corrigira esse bug primeiramente por possuir alta prioridade, pois afeta diretamente a integridade dos dados e a regra de negócio do sistema. Permitir múltiplas contas com o mesmo e-mail pode causar problemas de autenticação, inconsistência de dados e impactar a experiência do usuário.

Cenário 2

Em seguida corrigira esse bug por também possui alta prioridade, pois permite o envio de dados inválidos para o sistema, o que pode comprometer a qualidade das informações armazenadas e gerar problemas futuros no uso da aplicação.

---

## Caso tenha, coloque suas sugestões de melhorias para essas telas.

•	Implementar validação em tempo real nos campos.

•	Exibir mensagens claras de erro abaixo dos campos quando os dados forem inválidos.

•	Padronizar alinhamento e tamanho dos inputs para manter consistência visual no formulário.

•	Adicionar feedback visual para confirmação de senha, indicando quando as senhas não coincidem.

•	Implementar verificação para impedir cadastro com e-mails já registrados.



