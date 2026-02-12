# PalacioPradaHoldings
Palacio Prada Holdings
import React, { useState } from "react";
import { motion } from "framer-motion";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Mail, Phone, Building2, Scale, Briefcase } from "lucide-react";

export default function PalacioPradaHoldings() {
  const whatsappLink = "https://wa.me/573163659004";
  const [form, setForm] = useState({ nombre: "", email: "", mensaje: "" });

  const handleChange = (e) => {
    setForm({ ...form, [e.target.name]: e.target.value });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    window.location.href = `mailto:gerentephcali@gmail.com?subject=Contacto Ejecutivo - ${form.nombre}&body=${form.mensaje} - ${form.email}`;
  };

  return (
    <div className="bg-white text-[#0B2A4A] font-sans">
      {/* HEADER */}
      <header className="fixed top-0 w-full bg-white/90 backdrop-blur-md border-b border-[#C6A052]/30 z-50 shadow-sm">
        <div className="max-w-7xl mx-auto flex justify-between items-center px-6 py-4">
          <img src="/PALACIO PRADA HOLDINGS.jpg" alt="Logo Palacio Prada Holdings" className="h-14" />
          <nav className="hidden md:flex gap-10 text-sm font-medium tracking-wide">
            <a href="#firma" className="hover:text-[#C6A052] transition">La Firma</a>
            <a href="#servicios" className="hover:text-[#C6A052] transition">Servicios</a>
            <a href="#portafolio" className="hover:text-[#C6A052] transition">Portafolio</a>
            <a href="#legal" className="hover:text-[#C6A052] transition">Marco Legal</a>
            <a href="#liderazgo" className="hover:text-[#C6A052] transition">Liderazgo</a>
            <a href="#contacto" className="hover:text-[#C6A052] transition">Contacto</a>
          </nav>
        </div>
      </header>

      {/* HERO */}
      <section className="h-screen flex items-center justify-center text-center px-6 bg-gradient-to-b from-white via-[#F8F9FB] to-white">
        <motion.div initial={{ opacity: 0, y: 40 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 1 }} className="max-w-5xl">
          <h1 className="text-5xl md:text-7xl font-serif mb-6 tracking-wide">PALACIO PRADA HOLDINGS</h1>
          <div className="w-24 h-1 bg-[#C6A052] mx-auto mb-8"></div>
          <p className="text-lg md:text-xl text-gray-600 mb-10 leading-relaxed">
            Asambleas · Administración · Eventos<br />
            <span className="block mt-4 text-[#C6A052] font-semibold tracking-wide">Liderazgo en Gobernanza y Dirección Estratégica en Propiedad Horizontal</span>
            Firma especializada en estructuración institucional, gobierno corporativo y administración de alto nivel para copropiedades residenciales, mixtas y empresariales.
          </p>
          <Button className="bg-[#C6A052] text-white hover:bg-[#b8923f] px-10 py-6 text-lg rounded-2xl shadow-lg">
            Solicitar Asesoría
          </Button>
        </motion.div>
      </section>

      {/* FIRMA */}
      <section id="firma" className="py-28 px-6 max-w-6xl mx-auto text-center">
        <h2 className="text-4xl font-serif mb-6">Nuestra Firma</h2>
        <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
        <p className="text-gray-600 text-lg leading-relaxed">
          Palacio Prada Holdings es una firma de dirección estratégica enfocada en la transformación institucional de copropiedades y órganos de gobierno. Integramos disciplina jurídica, visión financiera y estructura corporativa para elevar la administración de propiedad horizontal a un modelo empresarial sólido, transparente y sostenible.
        </p>
      </section>

      {/* SERVICIOS */}
      <section id="servicios" className="bg-[#F8F9FB] py-28 px-6">
        <h2 className="text-4xl text-center font-serif mb-16">Servicios Corporativos</h2>
        <div className="grid md:grid-cols-3 gap-10 max-w-6xl mx-auto">
          {[{
            icon: <Building2 className="text-[#C6A052]" size={32} />, title: "Administración Estratégica", text: "Gestión integral con enfoque financiero, jurídico y preventivo." },
            { icon: <Briefcase className="text-[#C6A052]" size={32} />, title: "Asambleas Profesionales", text: "Dirección técnica bajo estándares de gobernanza." },
            { icon: <Scale className="text-[#C6A052]" size={32} />, title: "Consultoría P.H.", text: "Acompañamiento conforme a Ley 675 de 2001." }
          ].map((item, i) => (
            <motion.div key={i} whileHover={{ y: -8 }} transition={{ duration: 0.3 }}>
              <Card className="bg-white border border-[#C6A052]/20 rounded-2xl shadow-lg">
                <CardContent className="p-8 text-center">
                  <div className="mb-4 flex justify-center">{item.icon}</div>
                  <h3 className="text-lg mb-4">{item.title}</h3>
                  <p className="text-gray-600">{item.text}</p>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </div>
      </section>

      {/* PORTAFOLIO */}
      <section id="portafolio" className="py-28 px-6 max-w-6xl mx-auto text-center">
        <h2 className="text-4xl font-serif mb-6">Portafolio Institucional</h2>
        <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
        <p className="text-gray-600 text-lg">
          Dirección de asambleas, reestructuración administrativa, fortalecimiento de reglamentos internos y modernización financiera de copropiedades residenciales y mixtas.
        </p>
      </section>

      {/* MARCO LEGAL */}
      <section id="legal" className="bg-[#F8F9FB] py-28 px-6 max-w-6xl mx-auto text-center">
        <h2 className="text-4xl font-serif mb-6">Marco Legal y Gobierno Corporativo</h2>
        <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
        <p className="text-gray-600 text-lg leading-relaxed">
          Actuamos bajo el marco de la Ley 675 de 2001 y normativas complementarias, implementando principios de transparencia, control interno, responsabilidad fiduciaria y buenas prácticas de gobernanza.
        </p>
      </section>

      {/* LIDERAZGO */}
      <section id="liderazgo" className="py-28 px-6 max-w-5xl mx-auto text-center">
        <h2 className="text-4xl font-serif mb-6">Dirección Ejecutiva</h2>
        <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
        <p className="text-gray-600 text-lg leading-relaxed">
          Bajo el liderazgo de <strong>Eduardo Palacio Yanguas</strong>, la firma consolida estructuras administrativas sólidas con visión estratégica, disciplina jurídica y enfoque empresarial.
        </p>
      </section>

      {/* BLOG JURÍDICO */}
      <section id="blog" className="py-28 px-6 max-w-6xl mx-auto text-center">
        <h2 className="text-4xl font-serif mb-6">Artículos de Intereses</h2>
        <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
        <p className="text-gray-600 text-lg mb-12">
          Análisis especializados sobre propiedad horizontal, gobierno corporativo, responsabilidad de administradores y tendencias normativas.
        </p>
        <div className="grid md:grid-cols-3 gap-8">
          {["Responsabilidad del Administrador en PH","Claves para una Asamblea Exitosa","Gobernanza y Control Interno"].map((post,i)=>(
            <Card key={i} className="rounded-2xl shadow-md border border-[#C6A052]/20">
              <CardContent className="p-6">
                <h3 className="font-semibold mb-3">{post}</h3>
                <p className="text-gray-500 text-sm">Próximamente contenido especializado.</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      
      {/* CONTACTO */}
      <section id="contacto" className="bg-[#0B2A4A] py-24 px-6 text-white">
        <div className="max-w-4xl mx-auto text-center">
          <h2 className="text-4xl font-serif mb-6">Contacto Ejecutivo</h2>
          <div className="w-20 h-1 bg-[#C6A052] mx-auto mb-10"></div>
          <form onSubmit={handleSubmit} className="grid gap-6">
            <input type="text" name="nombre" placeholder="Nombre" onChange={handleChange} required className="p-4 rounded-xl text-black" />
            <input type="email" name="email" placeholder="Correo Electrónico" onChange={handleChange} required className="p-4 rounded-xl text-black" />
            <textarea name="mensaje" placeholder="Mensaje" rows="4" onChange={handleChange} required className="p-4 rounded-xl text-black"></textarea>
            <Button type="submit" className="bg-[#C6A052] hover:bg-[#b8923f] text-white py-4 rounded-2xl">Enviar Mensaje</Button>
          </form>
          <div className="mt-10 text-lg space-y-2">
            <div className="flex justify-center items-center gap-2"><Phone className="text-[#C6A052]"/> 316 365 9004</div>
            <div className="flex justify-center items-center gap-2"><Phone className="text-[#C6A052]"/> 320 519 9868</div>
            <div className="flex justify-center items-center gap-2"><Mail className="text-[#C6A052]"/> gerentephcali@gmail.com</div>
          </div>
        </div>
      </section>

      {/* BOTÓN WHATSAPP */}
      <a href={whatsappLink} target="_blank" rel="noopener noreferrer" className="fixed bottom-6 right-6 bg-[#25D366] text-white px-5 py-4 rounded-full shadow-xl text-sm font-semibold hover:scale-105 transition">
        WhatsApp Ejecutivo
      </a>

      <footer className="bg-white border-t border-[#C6A052]/30 py-8 text-center text-gray-500 text-sm">
        © 2026 Palacio Prada Holdings · Cali – Colombia · Versión Corporativa Premium
      </footer>
    </div>
  );
}
