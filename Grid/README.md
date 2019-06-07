PARENT

    display: grid/inline-grid;

    3x3
    grid-template-columns: auto auto auto; // rem/em/%/fr/repeat(2, 10px)
    grid-template-rows: auto auto auto; // -||-
    grid-auto-columns: 10px; /* No matter how many columns of content end up in the grid, each column will be this same width */
    grid-auto-rows: 1rem; /* No matter how many rows of content end up in the grid, each row will be this same height */

    grid-column-gap: 50px;
    grid-row-gap: 50px;
    grid-gap: 50px 100px; // Combine grid-column-gap and grid-row-gap
    grid-gap: 50px;

    justify-content: space-evenly/space-around/space-between/center/start/end
    align-content: -||-

    align-items: start/end/center/strech // Vertical
    justify-items: -||- // Horizontal

CHILD

    grid-column-start: 1; // from 1
    grid-column-end: 3; // up to 3
    grid-row-start: 1;
    grid-row-end: 3;

    grid-column: 1 / span 3; // grid-column-start grid-column-end
    grid-row: 1 / 4; // grid-row-start grid-row-end properties

    grid-area: 1 / 2 / 5 / 6; // grid-row-start, grid-column-start, grid-row-end and the grid-column-end

    align-self: start/end/center/strech
    justify-self: -||-

NAMING CHILD - PARENT

    grid-template-areas:
            'header header header header header header'
            'menu main main main right right'
            'menu footer footer footer footer footer';

NAMING CHILD - CHILD

    grid-area: menu;
    grid-area: main;
    
ORDER CHILD - PARENT

    grid-template-columns: auto auto auto;

ORDER CHILD - CHILD

    grid-area: 1 / span 3 / 2 / 1;  // grid-row-start, grid-column-startgrid-row-end and the grid-column-end
    grid-area: 3 / 3 / 4 / 4;
