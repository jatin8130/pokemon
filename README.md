Approach : 
For this project, I built upon the base from Assignment 1 and developed a full-featured Pokémon Explorer web app. I focused on maintaining a clean folder structure from the start, organizing code into separate folders like components, hooks, contexts, and pages.

I used React Context API to manage global state for favorites, and created a custom useLocalStorage hook to persist that data even after refresh.

Navigation between pages (Home, Detail, Favorites, Compare) was handled using React Router.

On the home page, I implemented filtering by multiple types, sorting (by ID and name), and pagination with configurable page sizes. I also used useMemo to keep the filtering and sorting fast.

The detail page shows complete info including stats, abilities, and evolution chain — the evolution part was tricky due to the nested structure of PokeAPI.

A comparison panel lets users compare two Pokémon side by side based on stats.

The UI was styled using Tailwind CSS and made responsive for mobile screens. I added a collapsible header with a dark theme that adapts on smaller screens.

Challenges Faced : 
Parsing Evolution Chains: PokeAPI returns deeply nested evolution data, so extracting the correct info required writing a recursive parser.

LocalStorage Sync: Getting the favorites state to stay in sync with localStorage was a bit tricky, especially ensuring it updates immediately and reliably.

Performance Optimization: With a lot of data on the list page, I noticed slow re-renders. Adding useMemo and useCallback helped improve performance.

Responsive Design: Making sure the layout and header worked properly across different screen sizes took some testing and adjustment.
