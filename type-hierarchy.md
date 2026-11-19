Understanding Any, Unknown, and Never in TypeScript

Developers can build safer and more dependable code thanks to TypeScript's robust type system. Any, unknown, and never are three significant types in its type hierarchy. Despite their apparent similarities, they serve distinct functions. any and unknown is known as top types and on the other hand never is known as bottom type.

1. Any Type

TypeScript's type checking for a specific value is disabled by the any type. Any kind of data may be assigned to any variable, and operations can be carried out without compiler problems.

let value: any = "Hello";
value = 100;
value.toUpperCase();

However, because TypeScript is unable to confirm the validity of an operation, this flexibility may result in runtime issues.

2. Unknown Type

Like any other type, the unknown type can hold any kind of value. However, before carrying out any activities, we must verify its kind.

let value: unknown = "Hello";

if (typeof value === "string") {
    console.log(value.toUpperCase());
}

Because type verification is necessary before accessing properties or invoking methods, unknown is thus safer than any.

3. Never Type

Values that never happen are represented by the never type. It is frequently applied to functions that either never complete running or consistently throw an error.

function throwError(): never {
    throw new Error("Something went wrong");
}

Summarization

any, unknown, and never fulfill distinct functions. Any eliminates type safety, unknown never represents impossible values, and type checking maintains type safety. When a value's true type is uncertain or actual type of a value is not known, developers should use unknown over any.