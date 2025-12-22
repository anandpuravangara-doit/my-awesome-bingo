

# Soc Ops Bingo — Copilot Instructions

## Mandatory Development Checklist
- [ ] `npm run lint` (if configured)
- [ ] `npm run build`
- [ ] `npm run test` (if tests are added)

## Quickstart & Structure
- React + TypeScript (Vite) social bingo game; all logic is client-side
- Key files:
  - `src/components/`: UI (BingoBoard, BingoSquare, GameScreen, StartScreen, BingoModal)
  - `src/data/questions.ts`: Bingo prompts
  - `src/hooks/useBingoGame.ts`: Game state logic
  - `src/utils/bingoLogic.ts`: Win checks, board generation
  - `src/index.css`: Tailwind v4 styles/tokens
  - `.lab/GUIDE.md`: Agentic workflows, workshop guide
  - `.github/instructions/`: Tailwind v4 & frontend design rules

## Core Patterns
- Component-driven UI, state via hooks
- Game state in `useBingoGame.ts`; questions from `questions.ts`
- Extend modes via new components/hooks (see GUIDE.md)
- No backend/API calls

## Workflows
- Install: `npm install`
- Dev: `npm run dev` (hot reload)
- Build: `npm run build`
- Test: add tests in `src/utils/bingoLogic.test.ts` (no runner preconfigured)
- Deploy: push to `main` → auto GitHub Pages

## Conventions
- Update questions in `src/data/questions.ts` or use Quiz Master agent
- Follow `.github/instructions/frontend-design.instructions.md` for creative UI
- Use Tailwind v4, see `.github/instructions/tailwind-4.instructions.md`

## Agents
- Quiz Master: creative prompts/questions
- Pixel Jam: UI/UX/design reviews
- TDD Red/Green/Refactor: test-driven features

---
See `.lab/GUIDE.md` and `.github/instructions/*` for details.
