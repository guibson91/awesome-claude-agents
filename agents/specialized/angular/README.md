# Angular Specialized AI Agents

Enterprise-grade Angular AI agents designed for modern Angular 19+ development with comprehensive
best practices, clean code principles, and production-ready patterns.

## 🎯 Agent Overview

### 1. **Angular Architect** (`@angular-architect`)

**Primary Angular development agent - Use for all general Angular work**

- ✅ Component architecture (Smart/Presentational patterns)
- ✅ Standalone components (Angular 19+ default)
- ✅ Signals and computed values
- ✅ Modern control flow (@if, @for, @switch)
- ✅ Dependency injection with inject()
- ✅ Routing and guards
- ✅ gRPC-Web integration
- ✅ Service-based state management
- ✅ Performance optimization (OnPush, lazy loading)

**When to use:**

- Creating new components or features
- Implementing business logic
- Setting up routing and navigation
- Integrating with gRPC services
- Architectural decisions

**Example usage:**

```
@angular-architect Create a subscription management dashboard with AG Grid,
reactive forms, and gRPC integration following the existing project patterns
```

---

### 2. **Angular RxJS Expert** (`@angular-rxjs-expert`)

**Reactive programming specialist - Use for complex async operations**

- ✅ Observable streams and operators
- ✅ State management with BehaviorSubject
- ✅ Error handling and retry logic
- ✅ Memory leak prevention
- ✅ Performance optimization (shareReplay, debounce)
- ✅ Advanced patterns (polling, caching, optimistic updates)
- ✅ Combination operators (combineLatest, forkJoin)

**When to use:**

- Complex observable compositions
- State management implementation
- Async operation handling
- Performance optimization of streams
- Memory leak debugging
- Real-time data synchronization

**Example usage:**

```
@angular-rxjs-expert Implement a real-time subscription status monitor with
polling, error handling, and optimistic updates using RxJS best practices
```

---

### 3. **Angular Testing Expert** (`@angular-testing-expert`)

**Testing specialist - Use for comprehensive test coverage**

- ✅ Unit testing (Jasmine/Karma)
- ✅ Component testing with TestBed
- ✅ Service testing with mocks
- ✅ Reactive forms testing
- ✅ Async operation testing
- ✅ Guard and directive testing
- ✅ Test coverage optimization
- ✅ TDD/BDD approaches

**When to use:**

- Writing unit tests for components
- Testing services and state management
- Testing reactive forms and validation
- Improving test coverage
- Debugging test failures
- Setting up testing infrastructure

**Example usage:**

```
@angular-testing-expert Write comprehensive unit tests for the subscription
service including gRPC calls, error handling, and state management
```

---

### 4. **Angular Material UI Expert** (`@angular-material-ui-expert`)

**UI/UX specialist - Use for Material Design and component styling**

- ✅ Angular Material 19+ components
- ✅ Custom theming and styling
- ✅ Material + Tailwind integration
- ✅ Responsive design patterns
- ✅ Accessibility (WCAG compliance)
- ✅ Custom component libraries
- ✅ Data tables and complex layouts
- ✅ Dialog and stepper components

**When to use:**

- Implementing Material Design components
- Creating custom themes
- Building complex UI layouts
- Accessibility improvements
- Responsive design implementation
- Component library development

**Example usage:**

```
@angular-material-ui-expert Create a Material-themed subscription table with
sorting, filtering, pagination, and bulk actions following accessibility best practices
```

---

## 🏗️ Project-Specific Integration

These agents are specifically tailored for your tech stack:

### **Tech Stack Support**

- ✅ Angular 19.2 with TypeScript 5.8
- ✅ Angular Material 19.2
- ✅ Tailwind CSS 4.0
- ✅ RxJS 7.8
- ✅ gRPC-Web with Protocol Buffers
- ✅ AG Grid Angular 33.2
- ✅ AWS Cognito authentication
- ✅ Reactive Forms with validation libraries

### **Architecture Patterns**

- ✅ Standalone components (Angular 19+ approach)
- ✅ Smart/Presentational component pattern
- ✅ Service-based state management
- ✅ Path aliases (@components, @services, @proto)
- ✅ Multi-environment configuration
- ✅ gRPC microservices integration

### **Best Practices Built-In**

- ✅ Clean Code principles (SOLID, DRY, KISS)
- ✅ TypeScript strict mode
- ✅ OnPush change detection
- ✅ Memory leak prevention (takeUntilDestroyed)
- ✅ Proper error handling
- ✅ Comprehensive testing
- ✅ Accessibility compliance
- ✅ Performance optimization

---

## 🚀 Quick Start Guide

### 1. **For New Feature Development**

```
@angular-architect Create a new FAQ management feature with CRUD operations,
following the existing subscription management patterns
```

### 2. **For Complex State Management**

```
@angular-rxjs-expert Implement a centralized notification system with
real-time updates, error handling, and offline support
```

### 3. **For Testing Implementation**

```
@angular-testing-expert Add comprehensive test coverage for the payment
cycle tracking feature including edge cases and error scenarios
```

### 4. **For UI/UX Work**

```
@angular-material-ui-expert Redesign the subscribers report grid with
improved mobile responsiveness and Material Design components
```

---

## 🎨 Component Patterns

### Smart Component Example

```typescript
// Container component with business logic
@Component({
  selector: 'app-subscription-list',
  standalone: true,
  changeDetection: ChangeDetectionStrategy.OnPush,
})
export class SubscriptionListComponent {
  private subscriptionService = inject(SubscriptionService);
  private destroyRef = inject(DestroyRef);

  subscriptions = signal<Subscription[]>([]);
  loading = signal<boolean>(false);

  ngOnInit() {
    this.loadSubscriptions();
  }

  private loadSubscriptions(): void {
    this.loading.set(true);
    this.subscriptionService
      .listSubscriptions()
      .pipe(takeUntilDestroyed(this.destroyRef))
      .subscribe({
        next: (data) => this.subscriptions.set(data),
        error: (err) => this.handleError(err),
        complete: () => this.loading.set(false),
      });
  }
}
```

### Presentational Component Example

```typescript
// Pure UI component
@Component({
  selector: 'app-subscription-card',
  standalone: true,
  changeDetection: ChangeDetectionStrategy.OnPush,
})
export class SubscriptionCardComponent {
  @Input({ required: true }) subscription!: Subscription;
  @Output() edit = new EventEmitter<Subscription>();
  @Output() delete = new EventEmitter<Subscription>();
}
```

---

## 📋 Collaboration Workflow

### Multi-Agent Collaboration

These Angular agents work seamlessly with other project agents:

```
# Complex feature development
@tech-lead-orchestrator Plan a multi-step subscription renewal feature
↓
@angular-architect Implement the core subscription renewal logic
↓
@angular-rxjs-expert Optimize the renewal state management
↓
@angular-material-ui-expert Create the renewal UI components
↓
@angular-testing-expert Add comprehensive test coverage
↓
@code-reviewer Review the complete implementation
```

### Integration with Universal Agents

- **@tailwind-frontend-expert**: For advanced Tailwind CSS styling
- **@performance-optimizer**: For bundle size and runtime optimization
- **@api-architect**: For gRPC service design
- **@code-reviewer**: For quality assurance before merging

---

## 🔧 Configuration Examples

### Angular Module Structure

```
src/app/
├── components/          # Shared presentational components
├── pages/              # Smart container components
├── services/           # Business logic and state
│   ├── grpc-*.service.ts
│   └── *-state.service.ts
├── models/             # TypeScript interfaces
├── pipes/              # Custom pipes
├── directives/         # Custom directives
├── guards/             # Route guards
├── interceptors/       # HTTP/gRPC interceptors
└── proto/              # Generated Protocol Buffer files
```

### Path Aliases (tsconfig.json)

```json
{
  "compilerOptions": {
    "paths": {
      "@components/*": ["src/app/components/*"],
      "@services/*": ["src/app/services/*"],
      "@models/*": ["src/app/models/*"],
      "@pipes/*": ["src/app/pipes/*"],
      "@directives/*": ["src/app/directives/*"],
      "@proto/*": ["src/app/proto/*"]
    }
  }
}
```

---

## 📚 Additional Resources

### Documentation

- [Angular Official Docs](https://angular.dev)
- [Angular Material](https://material.angular.io)
- [RxJS Documentation](https://rxjs.dev)
- [AG Grid Angular](https://www.ag-grid.com/angular-data-grid/)

### Best Practices

- [Angular Style Guide](https://angular.dev/style-guide)
- [TypeScript Best Practices](https://www.typescriptlang.org/docs/handbook/declaration-files/do-s-and-don-ts.html)
- [RxJS Best Practices](https://rxjs.dev/guide/overview)
- [Accessibility Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)

---

## 🎯 Success Metrics

These agents are designed to help you achieve:

- ✅ **Clean Code**: Maintainable, readable, and well-organized
- ✅ **Performance**: Fast load times, optimized bundles, efficient rendering
- ✅ **Quality**: >80% test coverage, zero memory leaks
- ✅ **Accessibility**: WCAG AA compliance
- ✅ **Scalability**: Easy to extend and maintain
- ✅ **Developer Experience**: Clear patterns, good documentation

---

## 💡 Tips for Maximum Effectiveness

1. **Be Specific**: Provide context about your existing code structure
2. **Reference Patterns**: Mention similar features in your codebase
3. **State Requirements**: Clearly define functional and non-functional requirements
4. **Request Tests**: Always ask for test coverage alongside implementation
5. **Iterate**: Use multiple agents in sequence for complex features

---

**Ready to build enterprise-grade Angular applications with AI assistance!** 🚀

Choose the right agent for your task and let them guide you through best practices, clean code, and
production-ready implementations.
