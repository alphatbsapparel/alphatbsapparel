
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

export default function ClothingBrandSite() {
  return (
    <div className="min-h-screen bg-gradient-to-br from-pink-500 via-purple-500 to-indigo-500 text-white">
      {/* Navbar */}
      <nav className="flex justify-between items-center p-6">
        <h1 className="text-3xl font-extrabold">The Brightest Star Alpha</h1>
        <div className="space-x-6">
          <a href="#home">Home</a>
          <a href="#about">About</a>
          <a href="#shop">Shop</a>
          <a href="#contact">Contact</a>
        </div>
      </nav>

      {/* Hero Section */}
      <section id="home" className="flex flex-col items-center text-center py-24 px-4">
        <motion.h2
          initial={{ opacity: 0, y: 40 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.6 }}
          className="text-6xl font-black mb-6"
        >
          Wear Your Attitude
        </motion.h2>
        <p className="max-w-xl text-lg mb-8">
          Premium streetwear designed to stand out. Loud colors. Bold identity.
        </p>
        <Button className="bg-black text-white hover:bg-white hover:text-black rounded-2xl px-8 py