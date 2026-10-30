# Restaurant Table Arrangement

A web app that seats parties at the smallest free table that fits them, using a **sorted linked list**.

**Live demo:** _paste your GitHub Pages link here_

## DSA concept: Linked list

Each table is a node holding its id, seat count, the party sitting there (or `null`), and a pointer to the next table. The list is kept **sorted by seat count**, so walking from the head, the first free table with enough seats is automatically the **best fit** (it wastes the fewest seats).

| Operation | Use in the app | Time |
|-----------|----------------|------|
| `insertSorted` | Add a new table in its correct position | O(n) |
| `findFree` | Traverse to the first free table that fits the party | O(n) |
| `remove` | Delete a free table by relinking the previous node | O(n) |
| Traverse | Draw the floor and count free seats | O(n) |

No array shifting is needed: inserting or removing a table only changes one or two `next` pointers.

## Features
- Seat a party at the best-fit free table
- Free a table when guests leave
- Add tables of any size (inserted in sorted order) and remove free tables
- Counters for tables, occupied tables, and free seats, plus an operation log

## Run it
Open `index.html` in a browser. No install or build step.

## Tech
HTML, CSS, and vanilla JavaScript in a single file.
