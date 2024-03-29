# Recuperação de senha

**RF**

- O usuário deve poder recuperar sua senha informando seu e-mail;
- O usuário deve receber um e-mail com instruções de recuperação de senha;
- O usuário deve poder resetar sua senha;


**RNF**
- Utilizar Mailtrap para testar envios em ambiente DEV;
- Utilizar Amazon SES para envios em produção;
- O envio de e-mails deve acontecer em segundo plano (Background Job);


**RN**
- O link enviado por e-mail para resetar senha deve expirar em 2hs;
- O usuário precisa confirmar a nova senha ao resetar sua senha;


# Atualização de perfil
**RF**

- O usuário deve atualizar seu perfil (Nome, e-mail e senha);

**RNF**

**RN**

- O usuário não pode alterar seu e-mail para um e-mail já utilizado;
- Para atualizar a senha, o usuário deve informar a senha antiga;
- Para atualizar sua senha, o usuário precisa confirmar a nova senha;



# Painel do prestador
**RF**

- O usuário deve poder listar seus agendamentos de um dia específico;
- O prestador deve receber uma notificação sempre que houver um novo agendamento;
- O prestador deve poder visualizar as notificações não lidas.

**RNF**

- Os agendamentos do prestador devem ser armazenados em cache;
- As notificações do prestador devem ser armazenadas no MongoDB;
- As notificações do prestador devem ser enviadas em tempo real utilizando Socket.io;


**RN**

- A notificação deve ter um status de lida ou não-lida para que o prestador possa controlar;

# Agendamento de serviços

**RF**

- O usuário deve poder listar todos os prestadores de serviço cadastrados;
- O usuário deve poder listar os dias de um mês com pelo menos um horário disponível de um prestador;
- O usuário deve poder listar horários disponíveis de um dia específico de um prestador;
- O usuário deve poder realizar um novo agendamento com um prestador;

**RNF**

- A listagem de prestadores deve ser armazenada em cache;

**RN**

- Cada agendamento deve durar 1h;
- Os agendamentos devem estar disponíveis entre 8h às 18h (Primeiro às 08h e o último às 17);
- O usuário não pode agendar em um horário já ocupado;
- O usuário não pode agendar em um horário que já passou;
- O usuário não pode agendar um serviço consigo mesmo;

