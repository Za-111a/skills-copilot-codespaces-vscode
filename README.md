import React from "react";
import "tailwindcss/tailwind.css";

const maps = [
  "Dust2", "Mirage", "Inferno", "Nuke", "Overpass", "Vertigo", "Ancient", "Anubis"
];

const Home = () => {
  return (
    <div className="min-h-screen bg-gray-900 text-white p-6">
      <h1 className="text-4xl font-bold text-yellow-400 text-center mb-6">CS2CYBER</h1>
      <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        {maps.map((map, index) => (
          <div key={index} className="bg-gray-800 p-4 rounded-2xl shadow-lg text-center">
            <h2 className="text-2xl font-semibold mb-2">{map}</h2>
            <p className="text-sm text-gray-400">Server: {map} #1</p>
            <button className="mt-3 w-full bg-yellow-400 text-black hover:bg-yellow-500 py-2 px-4 rounded-lg">Join Server</button>
          </div>
        ))}
      </div>
    </div>
  );
};

export default Home;

// Tailwind konfiguratsiyasi uchun quyidagi qadamlarni bajaring:
// 1. "tailwindcss" ni o'rnating: npm install -D tailwindcss postcss autoprefixer
// 2. "npx tailwindcss init -p" ni ishga tushiring
// 3. tailwind.config.js faylida "content" qatorini sozlang:
// module.exports = { content: ["./src/**/*.{js,ts,jsx,tsx}"], theme: { extend: {} }, plugins: [], };
// 4. "globals.css" yoki "index.css" ga "@tailwind base; @tailwind components; @tailwind utilities;" qo'shing.
