# **Правила именования**

- используем БЭМ
```block__element--modifier```
```block-name__element-name--modifier-name```

- для компонентов используем PascalCase

```js
//Component
const TodoList = () => {
   //...
}
```

- для простых переменных, имен функций, хуков и свойств объекта используем camelCase

```js
// Variable Name
const userName = "roscongress";
```

```js
// Function Name
const getFullName = (firstName, lastName) => {
    return `${firstName} ${lastName}`;
}
```

```js
// Object Properties
const user = {
  userName: "roscongress",
  firstName: "dev",
  lastName: "ops"
}
```

- для экспортируемых констант используем UPPER_CASE
```ts
  export const MAX_FILES_SIZE_MB = 10
```
- для enum используем UPPER_CASE
```ts
    enum RUNS_TYPE {
        CHECKLIST = 'checklist',
        CASE = 'case',
    }
```

- для интерфейсов используем PascalCase
```ts
    export interface StepObject {
        id: number;
        data: string;
    }
```

- для интерфейсов, работающих объектами, получаемыми с сервера использовать суффикс DTO
```ts
    export interface PermissionsDTO {
        access: boolean;
        users: number[];
        isAll?: boolean;
    }
```
- type использовать для создания псевдонимов более сложного типа в PascalCase

```ts
    export type GeneralizedStructure = Case | Checklist | Run;
    
    export type CreateRun = Partial<Run>;
```

- в названиях типов и интерфейсов суффиксы "Type" или "Interface" или префикс "I" не используется

- при создании кастомного валидатора для функции использовать суффикс Validate
```ts
  export const mustMatchValidate = (formGroup: UntypedFormGroup) =>  {
      ..........
      ..........
      return null;
  };
  ```

