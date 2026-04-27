- Usuário.
  
#### Fluxo principal:

- O usuário seleciona a opção “login usuário”.
  
- O sistema leva o usuário até a tela de registro contendo um formulário.
  
- O usuário preenche os campos do formulário (informando e-mail e senha).
  
- O sistema consulta o banco de dados para verificar a disponibilidade das informações fornecidas e se o usuário já possui uma matricula ativa.
  
- Se o usuario já possui uma matricula ativa o banco de dados retorna uma confirmação positiva e o usuário é levado a aréa o aluno.

- se a matricula do usuario tiver inativa ou vencida o usuário é levado a pagina de matricula para poder renova-la.

- Se o usuario não possui uma matricula aparece um modal com com dois botões ("sim" ou "não") na tela perguntando se o usuario deseja se matricular na academia.

- Se a reposta no modal for "sim" o sistema o leva a aréa de matricula.
  
- Se a resposta no modal for "não" o usuario volta a primeira pagina de cadastro.


- Usuário.
  
#### Fluxo principal:

- O usuário seleciona a opção “matricula”.

- O sistema leva o usuário até a tela de registro contendo um formulário.
  
- O usuário preenche os campos do formulário (informando: Nome, Idade, CPF, Email, dados do cartão e uma senha de acesso).

- O sistema salva os dados no banco de dados é apresenta uma mensagem de confirmação ("Parabéns matricula concluida!")

- o sistema leva o usuario a aréa do aluno.


- Usuário.
  
#### Fluxo principal:

- Ao entrar na aréa do aluno vai ter um carosel de fotos e uma aba superior com varios links para acessar as outras funções("Planilha de treino", "Aulas coletivas", "Conta" e "sobre nós")

- ao clicar em cada um os links vc é encaminhao para sua devida pagina.


- Usuário.
  
#### Fluxo principal:

- Ao clicar na opção de conta na areá do aluno vamos a uma pagina que temos uma tabela com as informações da matricula do usuáario.

- Ao fim da tabela tem duas opções ("editar" e "delete").

- Ao clicar na opção "editar" abri um modal com cada item da sua matricula para poder editar.

- Ao clicar na opção "deletar" abri um modal perguntando ("tem certeza se deseja excluir sua matrcula") com duas possiveis repostas("Sim" ou "Não").

