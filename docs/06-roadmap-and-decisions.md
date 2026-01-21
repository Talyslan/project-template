# 🛣️ Roadmap & Decisions

## Roadmap

### MVP (Minimum Viable Product)

- Core features implemented:
  - Task creation, update, deletion
  - List view and Kanban view
  - User authentication and account management
- Basic responsive UI
- Basic database structure and relationships

### Next (Short-term improvements)

- Enhanced filtering and search
- User settings and preferences
- Activity log / history tracking
- Minor UI/UX enhancements

### Future (Long-term ideas)

- Team collaboration and shared tasks
- Notifications and reminders
- Advanced analytics and reporting
- Mobile app or PWA version
- Third-party integrations

## Architectural Decisions

- **Frontend framework:** Chosen for component reusability and maintainability  
- **Backend structure:** API-first approach to separate concerns and enable future scaling  
- **Database:** Relational model for structured data, chosen for simplicity and integrity  
- **State management:** Selected to handle global state efficiently across views

## Trade-offs

- **Kanban + List Views** vs **more visualization options:**  
  Focused on simplicity and fast MVP delivery  
- **Relational DB** vs NoSQL:  
  Relational chosen for integrity and straightforward relationships  
- **Single-user focus (MVP)** vs Multi-user collaboration:  
  Multi-user features postponed for short-term roadmap

## Assumptions

- Users prefer simple, focused tools over feature-heavy systems  
- MVP must be delivered quickly for testing and feedback  
- Core flows are prioritized; additional features are added after user validation  
- Security and data integrity are critical from the start
