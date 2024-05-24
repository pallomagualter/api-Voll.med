<h1 align="center">
  🏥 API Voll.med 🧑🏻‍⚕️
</h1>


<div align="center">
    <img alt="app-voll-med" title="app-voll-med" width="80%"
    src="https://github.com/pallomagualter/api-Voll.med/blob/main/imgVollMed.png" />
</div>
<br />    

> Projeto feito com o intuito de fixar conhecimentos sobre a linguagem Java utilizando o Spring Boot. Aplicando conhecimentos como:
>  - Criação de uma API Rest em Java com Spring Boot
>  - Desenvolver CRUDs utilizando o banco de dados MySQL
>  - Utilizar o Flyway como ferramenta de Migrations da API
>  - Realizar validações utilizando o Bean Validation
>  - Realizar paginação dos dados da API
>  - Boas práticas na API
>  - Tratamento de erros
>  - Autenticação/Autorização
>  - Tokens JWT


## 🎨 Layout
O layout da aplicação mobile está disponível neste link: [Figma](https://www.figma.com/file/N4CgpJqsg7gjbKuDmra3EV/Voll.med)


<div align="center">
  <sub>Built with 💜 by
    <a href="https://github.com/pallomagualter/">Palloma Gualter</a>
  </sub>
</div>

## :heavy_check_mark: Requisitos

### Médico


- [x] O sistema deve possuir uma funcionalidade de cadastro de médicos, na qual as seguintes informações deverão ser preenchidas:

    - Nome, E-mail, Telefone, CRM
    - Especialidade (Ortopedia, Cardiologia, Ginecologia ou Dermatologia)
    - Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)
    - Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.

- [x] Não é permitido cadastrar mais de um médico com o mesmo e-mail

- [x] Não é permitido cadastrar médico sem e-mail

- [x] O sistema deve possuir uma funcionalidade de listagem de médicos, na qual as seguintes informações, de cada um dos médicos cadastrados, deverão ser exibidas:

    - Nome, E-mail, CRM, Especialidade
    - A listagem deve ser ordenada pelo nome do médico, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.

- [x] O sistema deve possuir uma funcionalidade de atualização de dados cadastrais de médicos, na qual as seguintes informações poderão ser atualizadas:
    - Nome, Telefone e Endereço
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - Não permitir a alteração do e-mail do médico;
        - Não permitir a alteração do CRM do médico;
        - Não permitir a alteração da Especialidade do médico.

- [x] O sistema deve possuir uma funcionalidade que permita a exclusão de médicos cadastrados.
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - A exclusão não deve apagar os dados do médico, mas torná-lo como "inativo" no sistema.


### Paciente


- [x] O sistema deve possuir uma funcionalidade de cadastro de pacientes, na qual as seguintes informações deverão ser preenchidas:
    - Nome
    - E-mail
    - Telefone
    - CPF
    - Endereço completo (logradouro, número, complemento, bairro, cidade, UF e CEP)
    - Todas as informações são de preenchimento obrigatório, exceto o número e o complemento do endereço.
- [x] O sistema deve possuir uma funcionalidade de listagem de pacientes, na qual as seguintes informações, de cada um dos pacientes cadastrados, deverão ser exibidas:
    - Nome
    - E-mail
    - CPF
    - A listagem deve ser ordenada pelo nome do paciente, de maneira crescente, bem como ser paginada, trazendo 10 registros por página.
- [x] O sistema deve possuir uma funcionalidade de atualização de dados cadastrais de pacientes, na qual as seguintes informações poderão ser atualizadas:
    - Nome
    - Telefone
    - Endereço
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - Não permitir a alteração do e-mail do paciente;
        - Não permitir a alteração do CPF do paciente.
- [x] O sistema deve possuir uma funcionalidade que permita a exclusão de pacientes cadastrados.
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - A exclusão não deve apagar os dados do paciente, mas torná-lo como "inativo" no sistema.


### Consultas


- [ ] O sistema deve possuir uma funcionalidade que permita o agendamento de consultas, na qual as seguintes informações deverão ser preenchidas:
    - Paciente
    - Médico
    - Data/Hora da consulta
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - O horário de funcionamento da clínica é de segunda a sábado, das 07:00 às 19:00;
        - As consultas tem duração fixa de 1 hora;
        - As consultas devem ser agendadas com antecedência mínima de 30 minutos;
        - Não permitir o agendamento de consultas com pacientes inativos no sistema;
        - Não permitir o agendamento de consultas com médicos inativos no sistema;
        - Não permitir o agendamento de mais de uma consulta no mesmo dia para um mesmo paciente;
        - Não permitir o agendamento de uma consulta com um médico que já possui outra consulta agendada na mesma data/hora;
        - A escolha do médico é opcional, sendo que nesse caso o sistema deve escolher aleatoriamente algum médico disponível na data/hora preenchida.
- [ ] O sistema deve possuir uma funcionalidade que permita o cancelamento de consultas, na qual as seguintes informações deverão ser preenchidas:
    - Consulta
    - Motivo do cancelamento
    - As seguintes regras de negócio devem ser validadas pelo sistema:
        - É obrigatório informar o motivo do cancelamento da consulta, dentre as opções: paciente desistiu, médico cancelou ou outros;
        - Uma consulta somente poderá ser cancelada com antecedência mínima de 24 horas.


# 💻  Technologies
This project was made using the follow technologies:

* [Spring Boot 3](https://spring.io/projects/spring-boot)
* [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
* [Lombok](https://projectlombok.org/)
* [Flyway](https://flywaydb.org/)
* [MySQL](https://www.mysql.com/)
* [JPA/Hibernate](https://www.alura.com.br/apostila-java-web/uma-introducao-pratica-ao-jpa-com-hibernate)
* [Maven](https://maven.apache.org/)
* [Insomnia](https://insomnia.rest/)


# 👩🏻‍💻 How to run

### Clone Repository
```bash
git clone https://github.com/pallomagualter/api-Voll.med.git
```

Access API at
```
http://localhost:8080/
```

Made with love 💜 by [Palloma Gualter](https://github.com/pallomagualter) 🚀.
This project is under the [MIT license](./LICENSE).


Give a ⭐️ if this project helped you!