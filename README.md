# ⚛️ Smart React & TypeScript Snippets

A curated collection of VS Code snippets designed to accelerate modern React development.

This is not just a standard snippet library; it includes **intelligent casing transforms**. If you create a file named `results-filter-form.tsx` and run the component snippet, it automatically generates `ResultsFilterForm` without you typing a single extra character.

## 🚀 Features

- **Smart Casing:** Automatically converts kebab-case filenames (`user-profile-card.tsx`) into PascalCase component names (`UserProfileCard`).
- **Modern Stack:** Built for React 18+, TypeScript, and TanStack Query (v4/v5).
- **Clean Code:** Generates functional components with typed props interfaces by default.
- **Productivity:** Includes shortcuts for Console logs, Hooks, and Async components.

## 📦 Installation

1.  Copy the content of `vscode-react-ts-snippets.json` from this repository.
2.  In VS Code, press `Cmd+Shift+P` (Mac) or `Ctrl+Shift+P` (Windows).
3.  Type **"Configure User Snippets"**.
4.  Select **"typescriptreact"** (or `typescriptreact.json`).
5.  Paste the snippets inside the existing JSON object.

---

## ⚡ Complete Snippet Reference

### 1. Smart Components (Auto-Naming)

_These snippets read your filename (e.g., `my-component.tsx`) and generate the correct PascalCase component name (e.g., `MyComponent`)._

| Trigger      | Description                    | Output / Logic                                      |
| :----------- | :----------------------------- | :-------------------------------------------------- |
| **`rafce`**  | React Arrow Function Component | `const MyComponent = () => { ... }`                 |
| **`rafcep`** | React Arrow Function w/ Props  | Includes `type MyComponentProps` & typed props      |
| **`rfce`**   | React Function Component       | `function MyComponent() { ... }`                    |
| **`rfcep`**  | React Function w/ Props        | Includes `interface MyComponentProps` & typed props |

### 2. Async Components

_For server components or components handling async logic._

| Trigger      | Description                   | Output                                  |
| :----------- | :---------------------------- | :-------------------------------------- |
| **`arfce`**  | Async React Function          | `const Component = async () => { ... }` |
| **`arfcep`** | Async React Function w/ Props | Adds `type Props` to the async function |

### 3. React Hooks

_Fast shortcuts for the most common React hooks._

| Trigger   | Description   | Output                                         |
| :-------- | :------------ | :--------------------------------------------- |
| **`us`**  | `useState`    | `const [state, setState] = useState(initial);` |
| **`ue`**  | `useEffect`   | `useEffect(() => { ... }, [dependencies]);`    |
| **`ucb`** | `useCallback` | `useCallback(() => { ... }, [dependencies]);`  |
| **`umm`** | `useMemo`     | `useMemo(() => { ... }, [dependencies]);`      |

### 4. TanStack Query (React Query)

_Boilerplate for data fetching and mutation._

| Trigger   | Description                  | What it generates                                                  |
| :-------- | :--------------------------- | :----------------------------------------------------------------- |
| **`rqg`** | `useQuery` (Get Request)     | Fetch function + `useQuery` hook + Loading/Error states + Map loop |
| **`rqm`** | `useMutation` (Post Request) | Fetch function + `useMutation` hook + Form UI + Submit handler     |

### 5. Utilities

| Trigger  | Description | Output                               |
| :------- | :---------- | :----------------------------------- |
| **`cl`** | Console Log | `console.log('Value >>>>>', value);` |

---

## 💡 Usage Example

**Scenario:** You create a new file named `src/components/student-results-card.tsx`.

1.  Type `rafcep` inside the file.
2.  Press `Tab`.

**Result:**
The snippet reads the filename `student-results-card`, converts it to `StudentResultsCard`, and generates:

```tsx
type StudentResultsCardProps = {};

const StudentResultsCard = ({}: StudentResultsCardProps) => {
  return <div>StudentResultsCard</div>;
};

export default StudentResultsCard;
```
