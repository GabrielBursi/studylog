# **Descrição do Projeto**
Sistema de gestão de projetos ágeis com funcionalidades básicas do Jira, incluindo criação de tarefas, quadros Kanban, sprints e acompanhamento de progresso. Os usuários poderão:

- Criar e gerenciar projetos com times
- Organizar tarefas em quadros Scrum/Kanban
- Definir sprints e backlogs
- Atribuir tarefas com prioridades e etiquetas
- Visualizar métricas de progresso

**Motivações:**
- Aprofundar conhecimento em desenvolvimento full-stack
- Entender desafios de aplicações colaborativas em tempo real
- Praticar gestão de estado complexo em aplicações web
- Explorar padrões de design para interfaces de gestão de projetos

---

## **Stack Tecnológica Proposta**
### **Frontend**
- **Next.js**
- **TypeScript**
- **Estado Global**: Zustand
- **Estilização**: Tailwind CSS + Headless UI
- **Bibliotecas de UI**: Radix UI ou Shadcn/ui
- **Gráficos**: Recharts ou Visx
- **Drag and Drop**: DnD Kit ou react-beautiful-dnd

### **Backend**
- **Nest.js**
- **Prisma ORM**

### **Banco de Dados**
- **Relacional**: DynamoDB
- **Alternativa**: Firebase (Firestore + Auth)

### **Outras Tecnologias**
- **Autenticação**: NextAuth.js ou Clerk
- **Realtime**: WebSocket (Pusher/Socket.io) ou Supabase Realtime
- **Deploy**: Vercel (Front) + Render/Railway (Back)

## **Principais Funcionalidades**
1. **Gestão de Projetos**
   - Criação de times e projetos
   - Controle de permissões (Admin/Membro)
   - Templates pré-definidos (Scrum, Kanban)

2. **Quadro de Tarefas**
   - Sistema drag-and-drop para colunas
   - Tipos de tarefas personalizáveis (User Story, Bug, Task)
   - Filtros avançados (assignee, sprint, tags)
   - Timer para tarefa

3. **Gestão de Sprints**
   - Planejamento de sprints com capacidade estimada
   - Burndown charts
   - Retrospectivas simplificadas

4. **Colaboração em Tempo Real**
   - Atualizações simultâneas no quadro
   - Comentários em tarefas
   - Notificações de mudanças

5. **Relatórios**
   - Velocity tracking
   - Cumulative Flow Diagram
   - Lead time/Cycle time

---

## **Arquitetura Proposta**
```
┌─────────────┐     ┌─────────────┐     ┌─────────────┐
│   Frontend  │ ◄──►│   Backend   │ ◄──►│  Database   │
│  (Next.js)  │     │ (API REST)  │     │ (PostgreSQL)│
└──────┬──────┘     └──────┬──────┘     └─────────────┘
       │ WebSocket         │
┌──────▼──────┐            │
│  Realtime   │            │
│  Service    │◄───────────┘
└─────────────┘
```