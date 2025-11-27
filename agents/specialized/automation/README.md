# Automation Agents

Specialized agents for AI-powered automation, workflow orchestration, and intelligent system integration.

## Available Agents

### ai-automation-architect
**Expert AI automation architect** specializing in n8n, Dify, workflow orchestration, and LLM integrations.

**Use when you need to:**
- Build intelligent automation workflows with AI/LLM integration
- Design WhatsApp bots or chatbots with natural language understanding
- Create multi-platform integration systems (n8n, Dify, Make, Zapier)
- Implement RAG systems with vector databases
- Optimize existing automation workflows
- Integrate databases (Supabase, PostgreSQL) with automation platforms
- Deploy workflows on Railway, Digital Ocean, or Easypanel
- Build agent-based systems with tool use and function calling

**Key Capabilities:**
- 🤖 AI & LLM integration (OpenAI, Anthropic Claude, local models)
- 🔄 Workflow orchestration (n8n, Dify, Railway)
- 💬 Messaging platform integration (WhatsApp, Telegram, Slack)
- 🗄️ Database integration (Supabase, PostgreSQL, Redis)
- 🔐 Security & authentication implementation
- 📊 Monitoring, logging, and analytics
- ⚡ Performance optimization
- 🏗️ Ynovation infrastructure expertise

**Example Use Cases:**
```
User: "Create a WhatsApp bot that answers customer questions using AI"
→ ai-automation-architect designs complete flow with n8n/Dify + LLM integration

User: "Build a lead capture system that qualifies leads with AI"
→ ai-automation-architect creates multi-step workflow with AI scoring

User: "My Dify workflow is slow, help optimize it"
→ ai-automation-architect analyzes and improves performance
```

## Integration with Other Agents

### Delegates to:
- **Database architects** for schema design and optimization
- **Frontend specialists** (React/Vue) for dashboard interfaces
- **DevOps experts** for infrastructure scaling
- **Backend developers** for custom API endpoints

### Works well with:
- **tech-lead-orchestrator** for complex project planning
- **code-reviewer** for workflow logic validation
- **performance-optimizer** for bottleneck analysis
- **documentation-specialist** for workflow documentation

## Common Patterns

### AI Chatbot Pattern
```
Message Input → Validation → Context Retrieval → LLM Processing → Response
                   ↓            ↓                    ↓              ↓
              Error Check   Database Query      Prompt Eng.    Formatting
```

### Database Automation Pattern
```
Trigger → Query Data → Transform → AI Analysis → Update DB → Notify
            ↓             ↓           ↓            ↓           ↓
         Validation   Normalize   Insights    Conditional   Webhook
```

### Multi-Platform Integration
```
Source A ──┐
Source B ──┼──→ n8n Workflow ──→ Dify AI ──→ Action A
Source C ──┘                                  └──→ Action B
```

## Best Practices

### When using automation agents:

1. **Start with Clear Requirements**
   - Define trigger sources clearly
   - Map data flow end-to-end
   - Identify error scenarios

2. **Design for Reliability**
   - Always implement error handling
   - Add retry logic for external calls
   - Include fallback mechanisms

3. **Optimize for Performance**
   - Cache frequent responses
   - Use parallel execution where possible
   - Monitor execution times

4. **Secure Your Workflows**
   - Validate webhook signatures
   - Sanitize user inputs
   - Use environment variables for secrets

5. **Plan for Scale**
   - Design for horizontal scaling
   - Implement rate limiting
   - Monitor resource usage

## Tech Stack Reference

### Platforms
- **n8n**: Workflow automation (self-hosted or cloud)
- **Dify.ai**: LLM application framework
- **Railway**: Container orchestration
- **Make/Zapier**: No-code automation

### Databases
- **Supabase**: PostgreSQL with real-time features
- **Redis**: Caching and sessions
- **Qdrant/Pinecone**: Vector databases for RAG

### AI/LLM
- **OpenAI**: GPT models
- **Anthropic**: Claude models
- **Open source**: Llama, Mistral, etc.

### Infrastructure
- **Digital Ocean**: VPS hosting
- **Easypanel**: Application management
- **Nginx**: Reverse proxy
- **Docker**: Containerization

## Quick Start Examples

### Create a WhatsApp AI Bot
```
1. Use ai-automation-architect to design workflow
2. Set up webhook in n8n/Railway
3. Configure Dify for NLP processing
4. Store conversations in Supabase
5. Deploy and test
```

### Build a Lead Qualification System
```
1. Connect form webhook to n8n
2. Extract and validate lead data
3. Send to Dify for AI scoring
4. Store qualified leads in Supabase
5. Trigger email notifications
```

### Implement RAG-based FAQ Bot
```
1. Prepare knowledge base documents
2. Generate embeddings (Dify/custom)
3. Store in vector database
4. Create retrieval workflow in n8n
5. Integrate with messaging platform
```

## Resources

### Documentation
- [n8n Documentation](https://docs.n8n.io)
- [Dify Documentation](https://docs.dify.ai)
- [Supabase Documentation](https://supabase.com/docs)
- [Railway Documentation](https://docs.railway.app)

### Related Files
- `../core/code-reviewer.md` - For workflow logic review
- `../core/performance-optimizer.md` - For optimization
- `../orchestrators/tech-lead-orchestrator.md` - For complex projects

---

**Note**: Automation agents are designed to work with the Ynovation infrastructure but can be adapted to any automation stack. Always test workflows thoroughly before production deployment.
