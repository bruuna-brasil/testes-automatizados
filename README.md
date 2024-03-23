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

   ```javascript
   it('should fetch all lessons', async () => {
     // Simular dados retornados do banco de dados
     const lessons = await LessonService.getAllLessons();
     expect(lessons.length).toBe(1); // Verifica se a função retornou uma aula
     // Adicione mais asserções conforme necessário para validar os dados das aulas retornadas
   });
   ```

   ```javascript
   it('should get lesson by class', async () => {
     // Simular dados retornados do banco de dados
     const lessonId = 1;
     const lessons = await LessonService.getLessonByClass(lessonId);
     expect(lessons.length).toBe(1); // Verifica se a função retornou uma aula
     // Adicione mais asserções conforme necessário para validar os dados das aulas retornadas
   });
   ```

   ```javascript
   it('should get lesson by id', async () => {
     // Simular dados retornados do banco de dados
     const lessonId = 1;
     const lesson = await LessonService.getLessonById(lessonId);
     expect(lesson.id_aula).toBe(1); // Verifica se a função retornou a aula correta
     // Adicione mais asserções conforme necessário para validar os dados da aula retornada
   });
   ```

Estes testes garantem que as funcionalidades relacionadas às aulas da ONG Gerando Falcões estejam funcionando conforme o esperado, ajudando a manter a qualidade e confiabilidade do sistema. Além disso, esses testes já estão presentes no projeto e rodam com sucesso.