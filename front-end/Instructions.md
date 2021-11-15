# Strapi Front-End Test

Hi the assignment consists of developing the homepage of a space trip booking application.

> Here is some information and requirements in order to successfully submit your application.

## Back-end

- Refer to [Backend Setup](BACK-END_SETUP.md)
- As the back-end runs on the 3000 port, you should start your back-end first.
- Endpoint `http://localhost:3000/graphql` to provide to your `apolloClient`.
- The graphQL playground is available at `http://localhost:3000/graphql`.
- To use the playground, you will need to configure the HTTP Headers (it will be the same in your `apolloClient`'s `authLink`)

```
{
  "Authorization": "Bearer API_KEY"
}
```

## Requirements

You only need to design the Map view and the Space center List view specified in the homepage design.

### Routing

Even though you need to develop and design only the homepage, you need to setup the routing for 2 views:

- Homepage: `path="/"`
- SpacenterPage: `path="/:id"`

---

### Technical stack

- [Create React App](https://create-react-app.dev/)
- [GraphQL](https://www.apollographql.com/docs/react/)
- [React Map GL](https://visgl.github.io/react-map-gl/)
- [Styled Components](https://www.styled-components.com)

---

### Design

You can use the design available [here](https://www.figma.com/file/Yb5aiTKi0CimdwdcfEsaSl/%5BDEV%5D-Strapi-technical-test?node-id=4%3A1)

To access the design, use the menu on the top left corner.

### Miscellaneous

- You must use apollo
- You must use react-map-gl
- You must setup the application's routing
- All your styling must be made with styled-components

---

## Quick Interactions Overview

You will need to develop several components but here are the expected interactions between them:

- `<Map />` <=> `<List />`
- `<List />` => `<Map />`

---

## Specifications

### Map

The Map is responsible for providing the coordinates (lat, lng) to perform a bounding-box.

#### Requirements

- When the user clicks on a marker from the map, the list must be scrolled to the clicked element and the card's rocket must bounce for 3s
- When the user clicks on a marker from the map, the map must center on the marker
- When the user clicks on a marker from the map, it must display a popup with the space center's name
- `<GeolocateControl />` must be implemented (`react-map-gl` component)
- `<NavigationControl />`must be implemented (`react-map-gl` component)

---

### List

Each card of the list provides a way for the user to highlight a marker on the map and also to redirect the user to space center's flights list page (you don't have to develop that one).

#### Requirements

- When the user hovers over a card, it must change the color of its marker on the map
- When the user clicks on the `SEE ALL FLIGHTS` button, it must redirect the user to the space center's "flights list" page. (Empty page)
