PARENT
    display: grid/inline-grid;

    grid-template-columns: auto auto auto;

    grid-column-gap: 50px;
    grid-row-gap: 50px;
    grid-gap: 50px 100px; // Combine grid-column-gap and grid-row-gap
    grid-gap: 50px;

    justify-content: space-evenly/space-around/space-between/center/start/end
    align-content: -||-

CHILD
    grid-column-start: 1; // from 1
    grid-column-end: 3; // up to 3
    grid-row-start: 1;
    grid-row-end: 3;

    grid-column: 1 / span 3; // grid-column-start grid-column-end
    grid-row: 1 / 4; // grid-row-start grid-row-end properties

    grid-area: 1 / 2 / 5 / 6; // grid-row-start, grid-column-start, grid-row-end and the grid-column-end

NAMING CHILD
    PARENT
        grid-template-areas:
                'header header header header header header'
                'menu main main main right right'
                'menu footer footer footer footer footer';
    CHILD
        grid-area: menu;
        grid-area: main;
    
ORDER CHILD
    PARENT
        grid-template-columns: auto auto auto;
    CHILD
        grid-area: 1 / span 3 / 2 / 1;  // grid-row-start, grid-column-start, grid-row-end and the grid-column-end
        grid-area: 3 / 3 / 4 / 4;
