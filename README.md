# Museu Historico de Sao Jose

A responsive landing page for the Museu Historico de Sao Jose, a city history museum in Brazil. The site presents the museum through image galleries, video sections, and an interactive 360 degree 3D tour rendered in the browser.

## Tech stack

- Next.js 14 with the App Router
- React 18
- TypeScript
- Tailwind CSS
- Three.js for the 3D tour and 3D object viewer
- Embla Carousel for the interactive carousels
- Radix UI and shadcn/ui components
- lucide-react and react-icons for iconography

## What it does

- Home page with a mobile first responsive layout and museum introduction.
- Interactive 360 degree tour that maps a panoramic photo onto an inverted sphere with clickable info markers (`src/components/Tour3D.tsx`, page at `src/app/tour`).
- 3D object viewer that loads a GLTF model with orbit controls (`src/components/ThreeScene.tsx`, page at `src/app/exposicoes/three`).
- Collection pages showing museum pieces, including a full collection view (`src/app/acervo`).
- Exhibitions, articles, and piece of the month pages (`src/app/exposicoes`, `src/app/artigos`, `src/app/pecaMes`).
- Video gallery that plays museum videos in a responsive grid (`src/components/VideoGallery.tsx`, page at `src/app/videos`).
- About page describing the museum (`src/app/about`).
- Reusable UI: header, footer, interactive carousels, cards, and gallery sections.

Text and images are currently static mocks. The layout was designed so these can later be fed from an API.

## Running locally

Clone the repository:

```bash
git clone https://github.com/nicolasfvp/museum-3d-tour.git
cd museum-3d-tour
```

Install dependencies:

```bash
npm install
```

Start the development server:

```bash
npm run dev
```

Open `http://localhost:3000` in your browser.

To build and run a production version:

```bash
npm run build
npm run start
```

## Project structure

```
public/            Static assets (images, fonts, videos, 3D models)
src/app/           App Router pages (home, about, acervo, tour, exposicoes, videos, ...)
src/components/    Reusable components (Header, Footer, Tour3D, ThreeScene, carousels, ...)
src/components/ui/ shadcn/ui primitives (button, carousel)
src/lib/           Shared utilities
```

## Status

Personal and academic project. The interface is complete with static content, and it is prepared to be connected to an API for dynamic data in the future.

## License

Released under the MIT License. See the LICENSE file for details.
