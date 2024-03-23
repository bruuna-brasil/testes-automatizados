
# Testes Automatizados

Nesta pasta, estão dois testes automatizados criados para o projeto, ambos podem ser rodados utilizando `npm test`. O framework utilizado para os testes é o Jest, que é especializado em testes em JavaScript. A seguir, detalhamos o funcionamento de cada teste:

### Testes para LeaderService e LeaderController

Estes testes verificam o funcionamento correto das funcionalidades relacionadas aos líderes da ONG Gerando Falcões.

1. **Teste para LeaderService:**

   Este teste verifica se a função `getAllLeaders` do `LeaderService` retorna corretamente todos os líderes cadastrados.

   ```javascript
   it('should fetch all leaders', async () => {
     // Simular dados retornados do banco de dados
     const leaders = await LeaderService.getAllLeaders();
     expect(leaders.length).toBe(1); // Verifica se a função retornou um líder
     // Adicione mais asserções conforme necessário para validar os dados dos líderes retornados
   });
   ```

   ...

2. **Testes para LessonService:**

   Estes testes verificam o funcionamento correto das funcionalidades relacionadas às aulas da ONG Gerando Falcões.

   ```markdown
   ## Caso de Teste: Obter Aula por ID

   **Objetivo:** Verificar se a função `getLessonById` do `LessonService` retorna corretamente uma aula específica.

   **Pré-condição:** Existência de uma aula com ID válido no banco de dados.

   **Procedimento de Teste:**
   1. Chamar a função `getLessonById` do `LessonService` com o ID da aula a ser obtida.
   2. Capturar o resultado retornado pela função.

   **Resultado Esperado:** A função deve retornar a aula correspondente ao ID fornecido.

   **Resultado Obtido:** A função retornou corretamente a aula desejada.

   **Pós-condição:** Nenhuma alteração no estado do sistema, apenas a obtenção dos dados da aula.

   ```javascript
   it('should get lesson by id', async () => {
     // Simular dados retornados do banco de dados
     const lessonId = 1;
     const lesson = await LessonService.getLessonById(lessonId);
     expect(lesson.id_aula).toBe(1); // Verifica se a função retornou a aula correta
     // Adicione mais asserções conforme necessário para validar os dados da aula retornada
   });
   ```

   Adicione mais casos de teste conforme necessário para cobrir outras funcionalidades do `LessonService`.

Estes testes garantem que as funcionalidades relacionadas às aulas da ONG Gerando Falcões estejam funcionando conforme o esperado, ajudando a manter a qualidade e confiabilidade do sistema.
