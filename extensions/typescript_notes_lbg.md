
# Typescript Notes — LBG 20 June

- `tsconfig: "es5"`
- React runs in browser
  - Safari
  - Firefox: Spidermonkey?
  - Chrome: Chromium (also used by Edge)

- Typescript makes functions clearer.

## Basic Types in Typescript:
- `String`
- `Number`
- `Boolean`
- String Unions (`"Small"` or `"Medium"` or `"Large"`)

- Amazon Cognito not used because of reality of FSA regulations.

- **EmployeeBadge**: `?? ""` — if undefined, show `null`.

---

# Typescript Notes — 1 July 2024

- Typescript is referred to as "static testing."
- **TDD**: Snapshots are captured states of components that React can compare changes to.
  - `npm run test`
  - **Mocking**: recreating databases to test build-level code.
  - React Jest testing library: [Jest Snapshot Testing](https://jestjs.io/docs/snapshot-testing)

---

# LBG Notes Duncan — 3rd July

- LBG is nice & happy/dandy at first but everyone has sprint boards of tickets to complete.
- Testing with Jest in React.
- Styled Components.
- Naming syntax: `Alert.styled.tsx`

```typescript
export type AlertType = "error" | "warning" | "info" | "success";

const addTwoNumbers = (num1: number, num2: number: number): number => num1 + num2;
```

- **Optional Operator**:

```typescript
const addTwoNumbers = (num1: number, num2: number: number, num3?: number) => {
  return num1 + num2 + (num3 ?? 0);
};
```

- **3A's Testing**:
  1. Arrange
  2. Act
  3. Assert
- In the command line: `w > p >`

---

# Duncan Notes — 4th July

- Typescript, JSON, GET Request Notes, Async
  - `petstore.swagger.io`
  - [JSON to Typescript Tool](https://transform.tools/json-to-typescript)

---

# DEV Deployment Levels

1. Local
2. Development
3. Staging (for high-level managers/stakeholders)
4. Production/Live

Use `printenv` in macOS to see environment variables.

```bash
.env.local — to specify your own local variables
```

---

# Duncan TypeScript Notes — 8th July 2024

- Libraries: `axios`, `classNames`, `emotion`, `prismJS`
- **Employees Filter Feedback**: `11:16am`

```typescript
export type Team = "CL" | "CD&A" | "CM&P" | "CS&E";
export type Player = {
  id: number;
  firstName: string;
  surName: string;
  gender: "male" | "female";
  company: string;
  email: string;
  phone: string;
  address: string;
  team: Team;
};
```

- **React Native**:
  - `useRef`: Hook to access the DOM.
  - Example: `const inputRef = useRef(); ref={inputRef}`

---

# Typescript Roundup — 6th Aug

```typescript
export const chefJobTitle = [
  "Head Chef",
  "Sous Chef",
  "Executive Chef",
  "Station Chef",
  "Pastry Chef",
  "Sauce Chef",
] as const;

export type ChefJobTitle = (typeof chefJobTitle)[number];

export type Chef = {
  id: number;
  name: string;
  jobTitle: ChefJobTitle;
  michelinStars: 0 | 1 | 2 | 3;
  trainingProgress: number;
  isSelected: boolean;
};
```

---

# LBG Notes — 7th Aug (WFH)

- Lloyds has migrated ~20 customer journeys (out of 140).
- Positive experiences: 
  - Valuable time spent with Devansh.
  - Enjoy learning from Duncan and the Bristol office atmosphere.

---

# Admin Hub 1.0

- Figma drop for desktop: 12th September.
- BOS: 8th October, Lloyds: 10th October.
- Working on OKYC (permissions for account transactions).

---

# TypeScript & Backend Calls — 2nd Oct

- **Null vs. Undefined in Javascript**: [Stackoverflow](https://stackoverflow.com/questions/5076944/what-is-the-difference-between-null-and-undefined-in-javascript)
  - `undefined`: Variable declared but not assigned.
  - `null`: Represents no value.
