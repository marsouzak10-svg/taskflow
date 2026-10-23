# Taskflow · Gerenciador de tarefas

Aplicação web de tarefas feita com **JavaScript puro**, com lógica separada da interface, **testes automatizados** e **integração contínua** (GitHub Actions).

🔗 Demo: `https://SEU-USUARIO.github.io/taskflow/`

![print do app](docs/print.png)

## Funcionalidades
- Criar tarefas com título, prioridade (baixa, média, alta) e prazo
- Marcar como concluída e excluir
- Buscar e filtrar (todas, pendentes, concluídas)
- Ordenação por prioridade e destaque de tarefas atrasadas
- Barra de progresso
- Dados salvos no navegador (`localStorage`)
- Acessível: foco visível, rótulos ARIA, uso por teclado

## Tecnologias
HTML5, CSS3, JavaScript (ES2020), Node.js (test runner nativo), GitHub Actions.

## Estrutura
```
src/tasks.js     regras de negócio (funções puras, sem DOM)
src/app.js       interface e persistência
tests/           testes unitários
.github/         pipeline de CI
```

## Como rodar
```bash
git clone https://github.com/SEU-USUARIO/taskflow.git
cd taskflow
# abra o index.html no navegador
```

## Testes
Requer Node.js 18 ou superior.
```bash
npm test
```

## Decisões técnicas
- **Funções puras e imutabilidade:** `tasks.js` não altera os dados recebidos, o que facilita testar e evita bugs.
- **Separação lógica/UI:** a regra de negócio roda no Node sem navegador.
- **Segurança:** o texto digitado é inserido com `textContent`, evitando XSS.
- **CI:** cada push executa os testes automaticamente.

## Próximos passos
- [ ] Editar tarefas
- [ ] Categorias e etiquetas
- [ ] Exportar/importar JSON
- [ ] Versão em TypeScript

## Autor
SEU NOME · [LinkedIn](https://linkedin.com/in/SEU-PERFIL) · [GitHub](https://github.com/SEU-USUARIO)

Licença MIT.
