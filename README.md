# Notification Service 📩

## Descrição

Este projeto é um sistema de notificações baseado no padrão **Strategy** em **Spring Boot**. Ele permite o envio de notificações para diferentes canais de comunicação, como **Discord, Instagram, Twitter, Email e WhatsApp**, através de uma interface comum.

## 🚀 Funcionalidades

- **Envio de notificações para múltiplos canais.**
- **Padrão Strategy** para uma arquitetura escalável e flexível.
- **Validação de dados** usando Jakarta Validation.
- **Spring Boot 3** para desenvolvimento rápido e eficiente.

## 🛠️ Tecnologias Utilizadas

- **Java 17+**
- **Spring Boot 3**
- **Spring Web**
- **Jakarta Validation**
- **SLF4J Logger**
- **Map Strategy** para implementação dinâmica de estratégias.

## 📚 Estrutura do Projeto

```
src/
├── main/
│   ├── java/com/buildrun/buildrunstrategyinpractice/
│   │   ├── controller/          # Controlador REST
│   │   ├── service/             # Serviço de Notificações
│   │   ├── service/strategy/    # Estratégias de Notificação
│   │   ├── Application.java     # Classe principal
│   └── resources/
│       ├── application.yml      # Configuração do Spring Boot
```

## 🔧 Como Executar

1. **Clone o repositório**
   ```bash
   git clone https://github.com/username/notification-service.git
   cd notification-service
   ```

2. **Compile e instale as dependências**
   ```bash
   mvn clean install
   ```

3. **Execute a aplicação**
   ```bash
   mvn spring-boot:run
   ```

4. **Acesse a API**
   ```bash
   http://localhost:8080/v1/notifications
   ```

## 👀 Endpoints da API

| Método | Endpoint               | Descrição               |
|---------|------------------------|-------------------------|
| POST    | `/v1/notifications`     | Enviar uma notificação |

### 🔹 Exemplo de Requisição (POST `/v1/notifications`)
```json
{
  "channel": "email",
  "destination": "user@example.com",
  "message": "Olá! Esta é sua notificação."
}
```

## 🏗️ Estratégia de Notificação

O projeto segue o padrão **Strategy**, onde cada tipo de notificação é implementado separadamente e gerenciado por um `Map<String, NotificationStrategy>`:

### 📩 Estratégias disponíveis:

| Canal      | Classe                         |
|------------|--------------------------------|
| Discord    | `DiscordNotificationStrategy`  |
| Instagram  | `InstagramNotificationStrategy` |
| Twitter    | `TwitterNotificationStrategy`  |
| Email      | `EmailNotificationStrategy`    |
| WhatsApp   | `WhatsappNotificationStrategy` |

## 💡 Como Contribuir

1. Faça um **fork** do repositório.
2. Crie um **branch** para sua feature (`feature/minha-feature`).
3. **Commit** suas mudanças (`git commit -m "Adicionei uma nova feature"`).
4. Faça um **push** para o branch (`git push origin feature/minha-feature`).
5. Abra um **pull request**.

## 🐟 Licença

Este projeto é licenciado sob a **MIT License**.

## 👨‍💻 Autor

**Ednilson Chiziane**  
Apaixonado por desenvolvimento de software e boas práticas de código.

