# Anotações Projeto BD

### Objetivo
* Montar sistema de rede de ensino de cursos de níveis básico e técnico-profissionalizante para população em situação de vulnerabilidade social.
* A rede possui unidades em várias cidades, mas apenas 1 por bairro/região.

### Funcionalidades
* Registrar unidade
* Registrar aluno
* Registrar funcionário
    * Diferenciação entre funcionários e o cargo de professor.
* Registrar professor
    * Separar professor entre:
        * nível técnico (exige ensino superior)
        * nível básico (não exige ensino superior)
    * Um professor de nível técnico pode dar aulas de nível básico, mas não o contrário.
* Pode haver mais de uma unidade por cidade, mas limite de uma unidade por bairro/região
* Agregação <professor ministra disciplina>: _oferecimento_
    * Desta forma, é possível se manter o histórico

### Entidades
* **Aluno**:
    * **NroRegistro**
    * CPF
    * Nome
* **Funcionario**:
    * **NroRegistro**
    * CPF
    * Nome
* **Professor**:
    * **NroRegistro**
    * CPF
    * Nome
* **Curso técnico**:
    * **CodCurso**
    * CPF
    * Nome
* **Curso básico**:
    * **CodCurso**
    * NomeCurso
* **Disciplina**:
    * **CodDisc**
    * NomeDisciplina
    * Nível (básico ou técnico)
* **Unidade**:
    * chave: numero da unidade (??)
* **Bairro**:
    * _Qual chave?_
* **Cidade**:
    * _Qual chave?_

### Perguntas
* Por haver limite de 1 por bairro/região, bairro/região deve ser entidade?
* Como registrar local da unidade, garantindo o limite de 1 por bairro/região, permitindo que o sistema informe quais estados e cidades possuem unidades?
* Como lidar com herança
* Diferenciação entre funcionários e o cargo de professor: com ou sem herança?
* Como lidar com a diferenciação de professores técnicos e básicos?
