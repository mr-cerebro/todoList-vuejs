# ✅ Vue Task Manager (Tailwind + daisyUI)

Uma lista de tarefas (To-Do List) moderna e responsiva construída com **Vue 3**, utilizando o ecossistema **Tailwind CSS** e componentes **daisyUI**.

![Vue.js](https://img.shields.io/badge/vuejs-%2335495e.svg?style=for-the-badge&logo=vuedotjs&logoColor=%234FC08D)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![daisyUI](https://img.shields.io/badge/daisyui-5833ff?style=for-the-badge&logo=daisyui&logoColor=white)

## 🚀 Funcionalidades

- **Adicionar Tarefas:** Criação rápida com tecla `Enter` ou botão.
- **Marcar como Concluída:** Toggle de estado com feedback visual (riscado/opacidade).
- **Remover Tarefas:** Exclusão individual de itens.
- **Contador Dinâmico:** Monitoramento em tempo real de tarefas totais e concluídas.
- **Design Responsivo:** Interface adaptável para qualquer tamanho de tela.

## 🛠️ Tecnologias Utilizadas

- [Vue 3 (Composition API)](https://vuejs.org/) - Framework progressivo para interfaces.
- [Tailwind CSS](https://tailwindcss.com/) - Framework CSS utilitário para estilização rápida.
- [daisyUI](https://daisyui.com/) - Plugin de componentes para Tailwind que agiliza o design.
- [Vite](https://vitejs.dev/) - Ferramenta de build ultra-rápida.

## 📦 Como rodar o projeto

### Pré-requisitos

Certifique-se de ter o [Node.js](https://nodejs.org/) instalado em sua máquina.

### Instalação

1.Clone o repositório:

   ```bash
   git clone https://github.com/mr-cerebro/todoList-vuejs.git
   ```

2.Entra na pasta do projecto:

```bash
    cd todoList-vuejs
```

3.Instala as depedências

```bash
    npm install
```

4.Inicie o servidor de desenvolvimento:

```bash
    npm run dev
```

Abra o navegador no endereço indicado (geralmente ````http://localhost:5173````).

**Principais recursos utilizados**:
````v-model````: Faz a ligação bi-direcional entre o input de texto e a variável newTask, além de controlar o estado dos checkboxes.

- **Classes do daisyUI:**

    - ````card````, ````card-body````: Criam o container elegante.
    - ````input-bordered````: Estiliza o campo de texto.
    - ````btn-primary```` e ````btn-ghost````: Estilizam os botões com as cores do tema.
    - ````checkbox-success````: Um checkbox que fica verde quando marcado.

**Computed Properties**: Usamos computed para calcular automaticamente o total de tarefas e quantas estão prontas.

## Como funciona a reatividade no Vue 3

### Próximos Passos
Esta é uma versão base. Para deixá-la "nível produção", você pode:
- **LocalStorage**: Salvar as tarefas para que elas não sumam ao atualizar a página.
- **Filtros**: Adicionar abas para ver "Todas", "Pendentes" e "Concluídas".
- **Temas**: O daisyUI permite trocar o tema (dark/light) apenas mudando um atributo no HTML.