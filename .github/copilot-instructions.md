
# Soc Ops Bingo — Copilot Instructions

## Development Checklist
- [ ] `npm run lint` (if configured)
- [x] `npm run dev` (local dev server)
- [ ] `npm run test` (if tests are added)
- [x] `npm run build` (production build)

## Project Overview
- **Type:** React + TypeScript (Vite) social bingo game
- **Purpose:** In-person icebreaker; users find people matching prompts to complete a bingo row
- **No backend:** All logic is client-side; no API calls or server code

## Key Files & Structure
- `src/components/`: UI (BingoBoard, BingoSquare, GameScreen, StartScreen, BingoModal)
- `src/data/questions.ts`: Bingo prompts (edit to change questions)
- `src/hooks/useBingoGame.ts`: Central game state logic (board, progress, win detection)
- `src/utils/bingoLogic.ts`: Core bingo logic (win checks, board generation)
- `src/index.css`: Tailwind v4 styles and tokens
- `.lab/GUIDE.md`: Workshop/lab instructions, agentic workflows
- `.github/instructions/`: Tailwind v4 and frontend design rules

## Architecture & Patterns
- **Component-driven:** Each UI element is a React component; state managed via hooks
- **Game state:** Centralized in `useBingoGame.ts` (board, selected squares, win state)
- **Data flow:**
  - Questions loaded from `questions.ts`
  - Board generated at game start; user actions update state via hooks
- **Modes:** Extendable via new components/hooks (see GUIDE.md for Scavenger Hunt, Card Deck Shuffle)
- **Agents:** Custom agents (Quiz Master, Pixel Jam, TDD Red/Green/Refactor) automate creative, TDD, and design workflows

## Developer Workflows
- **Install:** `npm install`
- **Dev server:** `npm run dev` (Vite, hot reload)
- **Build:** `npm run build`
- **Test:** (Add tests in `src/utils/bingoLogic.test.ts` or similar; no test runner preconfigured)
- **Lint:** (Add lint config as needed; not preconfigured)
- **Deploy:** Push to `main` branch → auto-deploys to GitHub Pages

## Project Conventions
- **Questions:** Update or theme via `src/data/questions.ts` or use the Quiz Master agent
- **Frontend design:** Follow `.github/instructions/frontend-design.instructions.md` for creative, non-generic UI
- **Styling:** Use Tailwind v4, see `.github/instructions/tailwind-4.instructions.md` for tokens, patterns, and migration
- **Instructions:** Keep `.github/instructions/*` up to date with design and Tailwind rules

## Examples
- To add a new game mode: create a new component in `src/components/`, add state logic in `hooks/`, and update the start screen
- To update questions: edit `src/data/questions.ts` or use the Quiz Master agent

## Agentic Patterns
- **Background/Cloud agents:** Use for linting, creative content, or design tasks (see GUIDE.md)
- **TDD agents:** Use TDD Red/Green/Refactor for test-driven features (see GUIDE.md)
- **Design agents:** Use Pixel Jam for UI/UX reviews and creative redesigns

---
For more, see `.lab/GUIDE.md` and `.github/instructions/*`.
