"use client";
import React from "react";
import { motion } from "framer-motion";
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import {
  CheckCircle,
  Mail,
  Phone,
  MapPin,
  ArrowRight,
  HelpCircle,
  Users,
  FileQuestion,
  MessageCircle,
} from "lucide-react";

const site = {
  brand: {
    name: "Estudio Contable G&A",
    claim: "Hacemos simple lo que parece complicado",
    logoText: "G&A",
  },
  hero: {
    title: "Tu estudio contable de confianza",
    subtitle:
      "Brindamos soluciones contables, impositivas y laborales con transparencia, agilidad y compromiso.",
    ctaPrimary: { label: "Hacer consulta", href: "#contacto" },
    ctaSecondary: { label: "Sobre nosotros", href: "#nosotros" },
  },
  contact: {
    address: "Buenos Aires, Argentina",
    phone: "+54 9 11 3569-1174",
    email: "maxigamba15@gmail.com",
    whatsapp:
      "https://wa.me/5491135691174?text=Hola%20G&A,%20quiero%20hacer%20una%20consulta",
  },
};

export default function LandingGA() {
  return (
    <div className="relative min-h-screen w-full bg-neutral-950 text-white scroll-smooth">
      {/* NAV */}
      <header className="sticky top-0 z-30 backdrop-blur supports-[backdrop-filter]:bg-neutral-950/70">
        <nav className="mx-auto max-w-6xl px-4 py-3 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="size-9 rounded-2xl bg-neutral-800 grid place-items-center text-sm font-bold">
              {site.brand.logoText}
            </div>
            <div className="leading-tight">
              <div className="font-semibold">{site.brand.name}</div>
              <div className="text-xs text-neutral-300">
                {site.brand.claim}
              </div>
            </div>
          </div>
          <div className="hidden md:flex items-center gap-4 text-sm">
            <a href="#nosotros" className="hover:text-white/90">
              Nosotros
            </a>
            <a href="#preguntas" className="hover:text-white/90">
              Preguntas
            </a>
            <a href="#novedades" className="hover:text-white/90">
              Novedades
            </a>
            <Button asChild className="rounded-2xl">
              <a href="#contacto">Consulta</a>
            </Button>
          </div>
        </nav>
      </header>

      {/* HERO */}
      <section className="relative overflow-hidden text-center md:text-left">
        <div className="absolute inset-0 bg-[radial-gradient(circle_at_top,rgba(255,255,255,0.08),transparent_60%)]" />
        <div className="mx-auto max-w-6xl px-4 pt-20 pb-16 grid md:grid-cols-2 items-center gap-10">
          <motion.div
            className="space-y-6"
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
          >
            <h1 className="text-4xl md:text-5xl font-semibold leading-tight">
              {site.hero.title}
            </h1>
            <p className="text-neutral-200 text-lg">{site.hero.subtitle}</p>
            <div className="flex flex-col sm:flex-row gap-3 justify-center md:justify-start">
              <Button asChild size="lg" className="rounded-2xl">
                <a href={site.hero.ctaPrimary.href}>
                  {site.hero.ctaPrimary.label}
                  <ArrowRight className="ml-2 w-4 h-4" />
                </a>
              </Button>
              <Button
                asChild
                size="lg"
                variant="secondary"
                className="rounded-2xl"
              >
                <a href={site.hero.ctaSecondary.href}>
                  {site.hero.ctaSecondary.label}
                </a>
              </Button>
            </div>
          </motion.div>

          <motion.div
            className="md:justify-self-end w-full text-center md:text-right"
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.8 }}
          >
            <h3 className="text-2xl font-semibold mb-2">
              {site.brand.claim}
            </h3>
            <p className="text-neutral-300">
              Confianza, cercanía y claridad en cada gestión.
            </p>
          </motion.div>
        </div>
      </section>

      {/* NOSOTROS */}
      <section id="nosotros" className="mx-auto max-w-6xl px-4 py-16 text-center md:text-left">
        <motion.h2
          className="text-2xl md:text-3xl font-semibold mb-6 flex items-center justify-center md:justify-start gap-2"
          initial={{ opacity: 0, y: 20 }}
          whileInView={{ opacity: 1, y: 0 }}
          viewport={{ once: true }}
        >
          <Users className="w-6 h-6" /> Sobre nosotros
        </motion.h2>
        <motion.p
          className="text-neutral-200 leading-relaxed max-w-3xl mx-auto"
          initial={{ opacity: 0 }}
          whileInView={{ opacity: 1 }}
          viewport={{ once: true }}
          transition={{ delay: 0.2 }}
        >
          En G&A somos un estudio contable con más de{" "}
          <strong>60 años de trayectoria</strong>, dedicado a brindar
          asesoramiento integral a empresas, profesionales y emprendedores. A
          lo largo de las décadas, acompañamos el crecimiento de nuestros
          clientes ofreciendo soluciones contables, impositivas y laborales con
          profesionalismo y compromiso.
        </motion.p>
      </section>

      {/* SERVICIOS */}
      <section
        id="servicios"
        className="mx-auto max-w-6xl px-4 py-16 text-center"
      >
        <motion.h2
          className="text-2xl md:text-3xl font-semibold mb-4 flex items-center justify-center gap-2"
          initial={{ opacity: 0, y: 20 }}
          whileInView={{ opacity: 1, y: 0 }}
          viewport={{ once: true }}
        >
          <FileQuestion className="w-6 h-6" /> Consultanos sobre nuestros
          servicios
        </motion.h2>
        <p className="text-neutral-200 max-w-2xl mx-auto mb-8">
          Cada cliente tiene necesidades únicas. Contanos tu situación y te
          asesoramos sobre el servicio contable más adecuado para vos o tu
          empresa.
        </p>
        <Button size="lg" className="rounded-2xl" asChild>
          <a href="#contacto">Hacer consulta</a>
        </Button>
      </section>

      {/* PREGUNTAS */}
      <section
        id="preguntas"
        className="mx-auto max-w-6xl px-4 py-16 text-left"
      >
        <h2 className="text-2xl md:text-3xl font-semibold mb-6 flex items-center gap-2">
          <HelpCircle className="w-6 h-6" /> Preguntas frecuentes
        </h2>
        <div className="grid gap-4 text-neutral-200">
          {[
            {
              q: "¿Atienden a personas de todo el país?",
              a: "Sí, trabajamos tanto de forma presencial como online, adaptándonos a las necesidades de cada cliente.",
            },
            {
              q: "¿Puedo derivar toda la gestión contable?",
              a: "Claro. Nos encargamos de la contabilidad, impuestos, liquidaciones y reportes mensuales.",
            },
            {
              q: "¿Qué documentación necesito para empezar?",
              a: "Con solo tu CUIT, constancia de inscripción y actividad, podemos iniciar el proceso de asesoramiento.",
            },
          ].map((faq, i) => (
            <motion.details
              key={i}
              className="bg-neutral-900/60 border border-neutral-800 rounded-2xl p-4"
              initial={{ opacity: 0, y: 10 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true }}
              transition={{ delay: i * 0.1 }}
            >
              <summary className="font-medium cursor-pointer">
                {faq.q}
              </summary>
              <p className="mt-2 text-sm text-neutral-300">{faq.a}</p>
            </motion.details>
          ))}
        </div>
      </section>

      {/* CONTACTO */}
      <section id="contacto" className="mx-auto max-w-6xl px-4 py-16">
        <div className="grid md:grid-cols-2 gap-8 items-center">
          <div>
            <h2 className="text-2xl md:text-3xl font-semibold mb-4 text-center md:text-left">
              Hacenos tu consulta
            </h2>
            <p className="text-neutral-200 mb-6 text-center md:text-left">
              Completá el formulario o escribinos directamente por WhatsApp.
              Te respondemos a la brevedad.
            </p>
            <div className="space-y-3 text-sm text-neutral-200">
              <div className="flex items-center gap-2 justify-center md:justify-start">
                <MapPin className="w-4 h-4" /> {site.contact.address}
              </div>
              <div className="flex items-center gap-2 justify-center md:justify-start">
                <Phone className="w-4 h-4" /> {site.contact.phone}
              </div>
              <div className="flex items-center gap-2 justify-center md:justify-start">
                <Mail className="w-4 h-4" /> {site.contact.email}
              </div>
            </div>
          </div>

          <Card className="bg-neutral-900/60 border-neutral-800 rounded-3xl">
            <CardContent className="p-6">
              {/* Formspree connection */}
              <form
                action="https://formspree.io/f/xbjnnggj"
                method="POST"
                className="grid gap-4"
              >
                <input
                  name="name"
                  required
                  className="bg-neutral-800/80 border border-neutral-700 rounded-2xl px-4 py-3 outline-none w-full text-white"
                  placeholder="Nombre"
                />
                <input
                  name="email"
                  type="email"
                  required
                  className="bg-neutral-800/80 border border-neutral-700 rounded-2xl px-4 py-3 outline-none w-full text-white"
                  placeholder="Email"
                />
                <textarea
                  name="message"
                  required
                  className="bg-neutral-800/80 border border-neutral-700 rounded-2xl px-4 py-3 outline-none w-full min-h-[120px] text-white"
                  placeholder="Contame tu consulta"
                ></textarea>
                <div className="flex flex-col sm:flex-row gap-3">
                  <Button type="submit" className="rounded-2xl">
                    Enviar
                  </Button>
                  <Button
                    asChild
                    variant="secondary"
                    className="rounded-2xl text-white"
                  >
                    <a
                      href={site.contact.whatsapp}
                      target="_blank"
                      rel="noreferrer"
                    >
                      WhatsApp
                    </a>
                  </Button>
                </div>
              </form>
            </CardContent>
          </Card>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="border-t border-neutral-800/70">
        <div className="mx-auto max-w-6xl px-4 py-8 text-sm text-neutral-300 flex flex-col md:flex-row items-center justify-between gap-2">
          <span>
            © {new Date().getFullYear()} Estudio Contable G&A. Todos los
            derechos reservados.
          </span>
          <a href="#" className="hover:text-white">
            Política de privacidad
          </a>
        </div>
      </footer>

      {/* BOTÓN FLOTANTE DE WHATSAPP */}
      <a
        href={site.contact.whatsapp}
        target="_blank"
        rel="noreferrer"
        aria-label="Contactar por WhatsApp"
        className="fixed bottom-6 right-6 bg-green-500 hover:bg-green-600 text-white p-4 rounded-full shadow-lg transition z-50"
      >
        <MessageCircle className="w-6 h-6 text-white" />
      </a>
    </div>
  );
}
