# unablazorlista12
# EcoMonitor - Lista 12 (Blazor)

Este projeto faz parte da Lista de Exercícios XII da disciplina de Interação Humano-Computador e UX. O objetivo foi criar uma interface gamificada para a ONG "ReCiclo", focada em registrar ações sustentáveis de forma simples e intuitiva.

## Identificação
- **Aluna:** Eduarda Cordeiro Furst Vieira.
- **Instituição:** Centro Universitário UNA - Campus Barreiro
- **Disciplina:** Interação Humano-Computador e UX
- **Professor:** Daniel Henrique Matos de Paiva

# Sobre o Projeto

O EcoMonitor é uma prova de conceito de gamificação para a ONG ReCiclo. Nesta aplicação, o usuário registra ações seguras e acompanha a pontuação acumulada em tempo real.
Cada ação é representada por um cartão reutilizável com:
- parâmetro de peso da ação;
- estado sonoro de pontuação;
- feedback visual de progresso e conquista.

##  Heurísticas de Nielsen Aplicadas

1. **Visibilidade do status do sistema**
Após cada clique no botão Registrar Atividade, o total acumulado é atualizado imediatamente, mostrando ao usuário o estado atual do sistema.

2. **Feedback imediato**
A interface responde instantaneamente à interação com atualização de contador, avanço da barra de progresso e mensagem de conquista ao atingir a meta.

3. **Consistência e padrões**
Os três cartões seguem o mesmo padrão visual e funcional, mudando apenas os parâmetros (título, peso e meta), o que reduz a carga cognitiva e facilita o uso.

##  Guia de Execução (Terminal)

### Pré-requisitos
- SDK do .NET instalado

### Passos
1. Restaurar:
   `dotnet restore`
2. Executar o projeto com perfil HTTPS:
   `dotnet run --launch-profile https`
3. Abrir no navegador o endereço informado no terminal:
   `https://localhost:PORTA`

##  Explicação Técnica sobre [Parâmetro]

O componente EcoStatus foi criado para ser reutilizável com parâmetros públicos:
- **Titulo**: definir o nome da ação sustentável.
- **PesoAcao**: define quantos pontos são aumentados por clique.
- **Meta**: defina o objetivo para destaque visual e mensagem de conquista.

Na página inicial, o mesmo componente é usado três vezes com valores diferentes. Isso permite reaproveitar estrutura e lógica sem duplicação de código.
Cada instância mantém seu próprio estado interno (TotalAcumulado), garantindo independência entre os cartões.

## Funcionalidades Implementadas

- Componente reutilizável com parâmetros personalizáveis
- Estado dinâmico por cartão
- Incremento por clique com base no peso da ação
- Estilização condicional ao atingir meta
- Barra de progresso
- Mensagem de conquista ao atingir a meta

## Resultado Esperado

O usuário consegue registrar ações sustentáveis em diferentes categorias e visualizar, em tempo real, sua evolução e impacto ambiental.

