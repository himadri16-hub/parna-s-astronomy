// Single-file React component (Tailwind CSS)
// How to use:
// 1) Create a new React app (Vite or Create React App) and install Tailwind CSS per the Tailwind docs.
// 2) Copy this component into a page (e.g. src/App.jsx) and ensure Tailwind is configured.
// 3) Deploy to Vercel/Netlify or export as static HTML.

import React from 'react';

export default function Website() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-800">
      {/* Header */}
      <header className="bg-white shadow-sm">
        <div className="container mx-auto px-6 py-5 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <div className="h-10 w-10 rounded-md bg-gradient-to-br from-indigo-500 to-purple-500 flex items-center justify-center text-white font-bold">AI</div>
            <div>
              <h1 className="text-lg font-semibold">YourSite</h1>
              <p className="text-xs text-gray-500">Design • Build • Launch</p>
            </div>
          </div>

          <nav className="hidden md:flex gap-6 items-center text-sm">
            <a href="#features" className="hover:text-indigo-600">Features</a>
            <a href="#examples" className="hover:text-indigo-600">Examples</a>
            <a href="#pricing" className="hover:text-indigo-600">Pricing</a>
            <a href="#contact" className="px-4 py-2 rounded-md bg-indigo-600 text-white hover:bg-indigo-700">Get started</a>
          </nav>

          <button className="md:hidden p-2 rounded-md bg-gray-100">☰</button>
        </div>
      </header>

      {/* Hero */}
      <section className="container mx-auto px-6 py-20 flex flex-col-reverse lg:flex-row items-center gap-10">
        <div className="lg:w-1/2">
          <h2 className="text-3xl md:text-4xl font-extrabold leading-tight">A beautiful, fast website—built for your needs.</h2>
          <p className="mt-4 text-gray-600">I’ll build a modern, responsive site using Tailwind and React, optimized for performance and conversions. Works great on mobile, tablet, and desktop.</p>

          <div className="mt-6 flex gap-3">
            <a href="#contact" className="inline-block px-6 py-3 bg-indigo-600 text-white rounded-md shadow-sm hover:bg-indigo-700">Hire me</a>
            <a href="#examples" className="inline-block px-6 py-3 border border-gray-200 rounded-md hover:bg-gray-100">See examples</a>
          </div>

          <ul className="mt-8 grid grid-cols-2 gap-3 text-sm text-gray-600">
            <li>✅ Responsive layout</li>
            <li>✅ SEO-friendly structure</li>
            <li>✅ Fast performance</li>
            <li>✅ Easy to update</li>
          </ul>
        </div>

        <div className="lg:w-1/2 flex justify-center">
          <div className="w-full max-w-md bg-white rounded-2xl shadow-lg p-6">
            <div className="h-48 bg-gradient-to-br from-indigo-400 to-purple-400 rounded-lg flex items-center justify-center text-white font-bold text-xl">Preview</div>
            <div className="mt-4 text-sm text-gray-600">This is a live preview box — replace with screenshots or interactive demo.</div>
          </div>
        </div>
      </section>

      {/* Features */}
      <section id="features" className="container mx-auto px-6 py-12">
        <h3 className="text-2xl font-bold">Features</h3>
        <p className="text-gray-600 mt-2">Everything you need to present your brand online.</p>

        <div className="mt-8 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">Fast & Lightweight</h4>
            <p className="text-sm text-gray-600 mt-2">Optimized bundles and lazy loading for fast page loads.</p>
          </div>
          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">SEO-Ready</h4>
            <p className="text-sm text-gray-600 mt-2">Semantic markup, meta tags, and sitemap if needed.</p>
          </div>
          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">Analytics</h4>
            <p className="text-sm text-gray-600 mt-2">Add Google Analytics, Plausible, or other tracking tools.</p>
          </div>
        </div>
      </section>

      {/* Examples / Portfolio */}
      <section id="examples" className="container mx-auto px-6 py-12">
        <h3 className="text-2xl font-bold">Examples</h3>
        <div className="mt-6 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
          {[1,2,3].map((n)=> (
            <article key={n} className="bg-white rounded-xl shadow-sm overflow-hidden">
              <div className="h-40 bg-gray-100 flex items-center justify-center text-gray-400">Project {n} image</div>
              <div className="p-4">
                <h4 className="font-semibold">Project Title {n}</h4>
                <p className="text-sm text-gray-600 mt-2">Short description of what I built — tech, scope, and result.</p>
              </div>
            </article>
          ))}
        </div>
      </section>

      {/* Pricing */}
      <section id="pricing" className="container mx-auto px-6 py-12">
        <h3 className="text-2xl font-bold">Pricing</h3>
        <p className="text-gray-600 mt-2">Simple pricing — pick a plan or request a custom quote.</p>

        <div className="mt-6 grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">Starter</h4>
            <p className="text-2xl font-bold mt-2">$299</p>
            <p className="text-sm text-gray-600 mt-2">One-page site, responsive design, contact form.</p>
            <button className="mt-4 w-full px-4 py-2 bg-indigo-600 text-white rounded-md">Choose</button>
          </div>

          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">Business</h4>
            <p className="text-2xl font-bold mt-2">$799</p>
            <p className="text-sm text-gray-600 mt-2">Multi-page site, CMS integration, SEO basics.</p>
            <button className="mt-4 w-full px-4 py-2 bg-indigo-600 text-white rounded-md">Choose</button>
          </div>

          <div className="p-6 bg-white rounded-xl shadow-sm">
            <h4 className="font-semibold">Custom</h4>
            <p className="text-2xl font-bold mt-2">Contact</p>
            <p className="text-sm text-gray-600 mt-2">Custom features, e-commerce, integrations.</p>
            <button className="mt-4 w-full px-4 py-2 bg-indigo-600 text-white rounded-md">Contact</button>
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="container mx-auto px-6 py-12">
        <h3 className="text-2xl font-bold">Contact</h3>
        <p className="text-gray-600 mt-2">Tell me about your project — timeline, budget, and goals.</p>

        <div className="mt-6 grid gap-6 lg:grid-cols-2">
          <form className="bg-white p-6 rounded-xl shadow-sm">
            <label className="block text-sm font-medium">Name</label>
            <input className="mt-1 w-full border border-gray-200 rounded-md p-2" placeholder="Your name" />

            <label className="block text-sm font-medium mt-4">Email</label>
            <input className="mt-1 w-full border border-gray-200 rounded-md p-2" placeholder="you@example.com" />

            <label className="block text-sm font-medium mt-4">Message</label>
            <textarea className="mt-1 w-full border border-gray-200 rounded-md p-2" rows={5} placeholder="Tell me about the project..." />

            <button type="submit" className="mt-4 px-4 py-2 bg-indigo-600 text-white rounded-md">Send</button>
          </form>

          <div className="bg-white p-6 rounded-xl shadow-sm">
            <h4 className="font-semibold">Quick info</h4>
            <p className="text-sm text-gray-600 mt-2">Prefer email? hello@yoursite.com</p>
            <p className="text-sm text-gray-600 mt-2">Based in: Remote</p>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-white border-t mt-12">
        <div className="container mx-auto px-6 py-6 flex flex-col md:flex-row items-center justify-between text-sm text-gray-600">
          <div>© {new Date().getFullYear()} YourSite — Built with ❤️</div>
          <div className="flex gap-4 mt-4 md:mt-0">
            <a href="#">Privacy</a>
            <a href="#">Terms</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
