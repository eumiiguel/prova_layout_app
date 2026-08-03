# Atividade PPDM - Programação para Dispositivos Móveis

## Parte 1: Respostas Conceituais

### 1. Diferença de Arquiteturas: Nativo vs. Cross-Platform (Flutter)
* **Desenvolvimento Nativo:** Desenvolve-se um aplicativo específico para cada plataforma usando suas linguagens e ferramentas oficiais (Kotlin/Java para Android; Swift/Objective-C para iOS). Garante acesso direto ao hardware, mas exige a manutenção de duas bases de código separadas.
* **Cross-Platform / Híbrido (Flutter):** Permite escrever um único código em Dart que é compilado diretamente para código de máquina (ARM) tanto no Android quanto no iOS. O Flutter usa seu próprio motor gráfico para desenhar a interface pixel por pixel, garantindo alto desempenho e consistência visual entre as plataformas.

---

### 2. Ciclo de Vida e Widgets: `StatelessWidget` vs. `StatefulWidget`
No Flutter, a interface é construída declarativamente usando Widgets.

* **StatelessWidget:** É um widget imutável (sem estado interno mutável). Uma vez construído, suas propriedades não se alteram durante a execução.
  * *Exemplo de uso:* Um texto fixo (`Text`), um ícone (`Icon`) ou um botão estático.
* **StatefulWidget:** É um widget dinâmico que mantém um objeto de estado (`State`). Suas informações internas podem mudar ao longo do tempo em resposta a ações do usuário ou chegada de dados.
  * *Exemplo de uso:* Um formulário de login, uma lista de itens favoritados ou um contador de cliques.

---

### 3. Gerenciamento de Estado: O que faz o `setState()`?
Quando invocamos o método `setState()`, notificamos o *framework* do Flutter de que o estado interno do widget foi alterado. Isso faz com que o Flutter reexecute o método `build()` daquele widget, redesenhando a interface gráfica na tela para refletir os novos dados atualizados.