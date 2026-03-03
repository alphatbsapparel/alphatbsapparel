import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function ClothingBrandSite() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-pink-500 via-purple-500 to-indigo-500 text-white">
      <nav className="flex justify-between items-center p-6">
        <h1 className="text-3xl font-extrabold">The Brightest Star Alpha</h1>
        <div className="space-x-6">
          <a href="#home">Home</a>
          <a href="#about">About</a>
          <a href="#shop">Shop</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>

      <section id="home" className="flex flex-col items-center text-center py-24 px-4">
        <motion.h2 initial={{ opacity: 0, y: 40 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }} className="text-6xl font-black mb-6">
          Wear Your Attitude
        </motion.h2>
        <p className="max-w-xl text-lg mb-8">
          Premium streetwear designed to stand out. Loud colors. Bold identity.
        </p>
        <Button className="bg-black text-white hover:bg-white hover:text-black rounded-2xl px-8 py-6 text-lg">
          Shop Now
        </Button>
      </section>

      <section id="about" className="py-20 px-6 bg-black/30">
        <h3 className="text-4xl font-bold mb-6">About Us</h3>
        <p className="max-w-3xl">
          The Brightest Star Alpha is a fashion-forward apparel brand blending street culture with fearless design. We believe clothing is a statement — not just an outfit.
        </p>
      </section>

      <section id="shop" className="py-20 px-6">
        <h3 className="text-4xl font-bold mb-10">Featured Products</h3>
        <div className="grid md:grid-cols-3 gap-6">
          {["Neon Hoodie", "Graphic Tee", "Urban Jacket"].map((item) => (
            <Card key={item} className="bg-white text-black rounded-2xl">
              <CardContent className="p-6">
                <div className="h-40 bg-gray-200 rounded-xl mb-4" />
                <h4 className="text-xl font-bold">{item}</h4>
                <p className="mb-4">$79</p>
                <Button className="w-full rounded-xl">Add to Cart</Button>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      <section id="contact" className="py-20 px-6 bg-black/40">
        <h3 className="text-4xl font-bold mb-6">Contact Us</h3>
        <form className="max-w-lg space-y-4">
          <input placeholder="Name" className="w-full p-3 rounded-xl text-black" />
          <input placeholder="Email" className="w-full p-3 rounded-xl text-black" />
          <textarea placeholder="Message" className="w-full p-3 rounded-xl text-black" />
          <Button className="rounded-xl px-6 py-4">Send Message</Button>
        </form>
      </section>

      <footer className="text-center py-6 bg-black/70">
        © 2026 The Brightest Star Alpha. All rights reserved.
      </footer>
    </div>
  );
}export function Card({ children, className }) {
  return <div className={`shadow-lg ${className}`}>{children}</div>;
}

export function CardContent({ children, className }) {
  return <div className={`p-4 ${className}`}>{children}</div>;
}export function Button({ children, className, onClick }) {
  return (
    <button className={`font-bold ${className}`} onClick={onClick}>
      {children}
    </button>
  );
}{
  "name": "alphatbsapparel",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  },
  "dependencies": {
    "framer-motion": "^10.12.16",
    "next": "13.5.5",
    "react": "18.2.0",
    "react-dom": "18.2.0"
  }
}/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./app/**/*.{js,jsx}", "./components/**/*.{js,jsx}"],
  theme: { extend: {} },
  plugins: [],
}module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}/** @type {import('next').NextConfig} */
const nextConfig = {
  reactStrictMode: true,
}

module.exports = nextConfig# The Brightest Star Alpha

Official website for The Brightest Star Alpha apparel brand.
