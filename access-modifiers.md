TypeScript OOP Access Modifiers

One key component of TypeScript's Object-Oriented Programming (OOP) is access modifiers. They regulate access to class methods and attributes. The three primary access modifiers offered by TypeScript are protected, private, and public. In order to stop property reassignment, it also offers readonly.

1. Public

The public modifier allows class properties and methods to be accessed from anywhere. It is also the default access modifier.

2. Private

The private modifier restricts access to the class where the property or method is declared. It cannot be accessed directly from outside the class or from a subclass.

3. Protected

The protected modifier allows access within the declaring class and its subclasses. However, it cannot be accessed directly from outside the class hierarchy.

4. Readonly

The readonly modifier prevents a property from being reassigned after initialization. It can be initialized when declared or inside the constructor.


class Employee {
    protected name: string;
    private salary: number;

    constructor(name: string, salary: number) {
        this.name = name;
        this.salary = salary;
    }

    public getDetails(): string {
        return `${this.name}: ${this.salary}`;
    }
}

class Manager extends Employee {
    getName(): string {
        return this.name;
    }
}

In this example, Manager can access name because it is protected, but it cannot directly access salary because it is private.

Conclusion

Access modifiers help developers achieve encapsulation, improve code organization, and control data access. Using them properly makes TypeScript applications more maintainable, structured, and reliable.