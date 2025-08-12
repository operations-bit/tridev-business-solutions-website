import React from "react";
import { motion } from "framer-motion";

export default function App() {
  return (
    <div className="font-sans bg-gray-50 text-gray-900">
      {/* Header */}
      <header className="bg-gradient-to-r from-teal-600 to-green-500 text-white p-6 flex justify-between items-center shadow-lg sticky top-0 z-50">
        <h1 className="text-2xl font-extrabold tracking-wide">Tridev Business Solutions</h1>
        <nav className="space-x-6 font-medium">
          <a href="#services" className="hover:text-yellow-300 transition">Services</a>
          <a href="#process" className="hover:text-yellow-300 transition">Process</a>
          <a href="#contact" className="hover:text-yellow-300 transition">Contact</a>
        </nav>
      </header>

      {/* Hero Section */}
      <section className="bg-gradient-to-r from-green-500 to-teal-600 text-white py-20 text-center relative overflow-hidden">
        <motion.h2 initial={{ opacity: 0, y: -20 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.6 }} className="text-5xl font-extrabold mb-4 drop-shadow-lg">
          Compliance Made Simple
        </motion.h2>
        <motion.p initial={{ opacity: 0 }} animate={{ opacity: 1 }} transition={{ delay: 0.3 }} className="max-w-2xl mx-auto text-lg leading-relaxed">
          We deliver fast, reliable, and hassle-free compliance services across India — from EPR to BIS, FSSAI, IEC, APEDA, and more.
        </motion.p>
        <motion.a whileHover={{ scale: 1.05 }} href="#contact" className="mt-8 inline-block bg-yellow-400 text-gray-900 px-8 py-3 rounded-full font-bold shadow-md hover:shadow-xl transition">
          Get a Free Consultation
        </motion.a>
      </section>

      {/* Services Section */}
      <section id="services" className="py-20 px-8 bg-white">
        <h2 className="text-4xl font-extrabold text-center mb-16 text-teal-700">Our Premium Services & Pricing</h2>
        <div className="grid gap-10 sm:grid-cols-2 lg:grid-cols-3">
          {[
            { title: 'EPR Compliance', price: '₹1,50,000/year', desc: 'Battery, Electronic & Plastic EPR compliance.' },
            { title: 'BIS & Product Approvals', price: '₹80,000', desc: 'ISI, CRS registrations and audit coordination.' },
            { title: 'FSSAI & IEC', price: '₹10,000', desc: 'Licensing and import/export code registration.' },
            { title: 'WPC Approvals & Wireless', price: '₹20,000', desc: 'ETA, wireless import licenses.' },
            { title: 'APEDA, Customs & Trade', price: '₹25,000', desc: 'Export registrations and documentation support.' },
            { title: 'Compliance Outsourcing', price: '₹2,00,000/year', desc: 'Annual filings and compliance management.' }
          ].map((service, i) => (
            <motion.div key={i} whileHover={{ scale: 1.05 }} className="bg-gradient-to-br from-white to-gray-50 p-8 rounded-2xl shadow-lg hover:shadow-2xl transition border border-gray-100">
              <h3 className="text-2xl font-bold text-teal-700 mb-2">{service.title}</h3>
              <p className="font-semibold text-xl text-yellow-500 mb-4">{service.price}</p>
              <p className="text-gray-600 leading-relaxed">{service.desc}</p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Process Section */}
      <section id="process" className="py-20 px-8 bg-gray-100">
        <h2 className="text-4xl font-extrabold text-center mb-16 text-teal-700">How We Work</h2>
        <div className="flex flex-wrap gap-8 justify-center">
          {[
            { step: 'Assessment', desc: 'We assess your compliance needs.' },
            { step: 'Documentation', desc: 'We prepare and verify all required documents.' },
            { step: 'Submission & Follow-up', desc: 'We submit applications and follow up until approval.' }
          ].map((p, idx) => (
            <motion.div key={idx} whileHover={{ y: -5 }} className="flex-1 min-w-[250px] bg-white p-8 rounded-2xl text-center shadow-md hover:shadow-xl transition border-t-4 border-teal-500">
              <div className="text-4xl font-extrabold text-yellow-500">{idx + 1}</div>
              <h3 className="mt-4 text-2xl font-semibold text-teal-700">{p.step}</h3>
              <p className="mt-2 text-gray-600 leading-relaxed">{p.desc}</p>
            </motion.div>
          ))}
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="bg-gradient-to-r from-teal-700 to-green-600 text-white py-16 px-8">
        <div className="grid gap-8 sm:grid-cols-2 lg:grid-cols-3">
          <div>
            <h3 className="text-2xl font-bold">Tridev Business Solutions</h3>
            <p className="mt-2 text-gray-200">Andheri, Mumbai • PAN India services</p>
            <p className="mt-1 text-gray-200">Phone: 9811226539</p>
            <p className="mt-1 text-gray-200">Email: info@tridev.co.in</p>
          </div>
          <div>
            <h4 className="font-semibold mb-2">Quick Links</h4>
            <a href="#services" className="block hover:text-yellow-300">Services</a>
            <a href="#process" className="block hover:text-yellow-300">Process</a>
            <a href="#contact" className="block hover:text-yellow-300">Contact</a>
          </div>
          <div>
            <h4 className="font-semibold mb-2">Request a Proposal</h4>
            <form className="space-y-3">
              <input placeholder="Company name" className="p-3 w-full rounded bg-gray-800 border border-gray-700 focus:outline-none focus:ring focus:ring-yellow-400" />
              <input placeholder="Email" className="p-3 w-full rounded bg-gray-800 border border-gray-700 focus:outline-none focus:ring focus:ring-yellow-400" />
              <button type="submit" className="bg-yellow-400 hover:bg-yellow-500 text-gray-900 px-4 py-3 rounded font-semibold w-full">Request Proposal</button>
            </form>
          </div>
        </div>
        <p className="text-center mt-8 text-sm text-gray-300">© {new Date().getFullYear()} Tridev Business Solutions — All rights reserved.</p>
      </footer>
    </div>
  );
}
