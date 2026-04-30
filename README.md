# Gallery Project

A React-based image gallery application that fetches and displays images from the Picsum Photos API with pagination support.

## Features

- **Dynamic Image Loading**: Fetches high-quality images from the [Picsum Photos API](https://picsum.photos/)
- **Pagination**: Navigate through multiple pages of images with Previous/Next buttons
- **Responsive Grid Layout**: Images displayed in a responsive grid with Tailwind CSS
- **Loading States**: Shows a loading indicator while fetching data
- **Clickable Images**: Each image links to the original source on Picsum Photos
- **Author Attribution**: Displays the photographer's name below each image

## Tech Stack

- **React** 19.2.5 - UI library
- **Vite** 8.0.9 - Build tool and development server
- **Axios** 1.15.2 - HTTP client for API calls
- **Tailwind CSS** 4.2.4 - Utility-first CSS framework
- **JavaScript (ES6+)** - Modern JavaScript

## Getting Started

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn

### Installation

1. Clone or download the project
2. Navigate to the project directory:
   ```bash
   cd gallery-project
   ```
3. Install dependencies:
   ```bash
   npm install
   ```

### Development

Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5173` (or another port if 5173 is in use).

## Available Scripts

- `npm run dev` - Start the development server with hot module reloading
- `npm run build` - Build the project for production
- `npm run preview` - Preview the production build locally
- `npm run lint` - Run ESLint to check code quality

## Project Structure

```
gallery-project/
├── src/
│   ├── App.jsx           # Main app component with pagination logic
│   ├── main.jsx          # React entry point
│   ├── index.css         # Global styles
│   └── components/
│       └── Card.jsx      # Image card component
├── index.html            # HTML entry point
├── vite.config.js        # Vite configuration
├── tailwind.config.js    # Tailwind CSS configuration
├── eslint.config.js      # ESLint configuration
└── package.json          # Project dependencies and scripts
```

## How It Works

1. **App.jsx** fetches images from Picsum Photos API (27 images per page)
2. **useState** manages the current page index and user data
3. **useEffect** triggers API calls whenever the page changes
4. Images are mapped and rendered as **Card** components
5. **Pagination buttons** control the page state
6. **Card.jsx** displays individual images with author names and links

## API Integration

The app uses the Picsum Photos API endpoint:
```
https://picsum.photos/v2/list?page={page_number}&limit=27
```

Each page returns 27 random images with metadata including:
- `url` - Link to the image on Picsum Photos
- `download_url` - Direct image URL
- `author` - Photographer's name

## Browser Support

Works on all modern browsers that support ES6 and React 19.

## License

This is a learning project from the React JS course.
