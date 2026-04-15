import { Link } from "react-router-dom";
import { Star, Wifi, Wind, ShieldCheck, MapPin, ArrowRight } from "lucide-react";
import heroImage from "@/assets/hero-hotel.jpg";
import roomImage from "@/assets/room-king.jpg";
import templeImage from "@/assets/ahobilam-temple.jpg";

/* ================= HEADER ================= */
const Header = () => (
  <header className="fixed top-0 left-0 w-full bg-background/90 backdrop-blur border-b border-border z-50">
    <div className="container mx-auto flex items-center justify-between p-4">
      <h1 className="text-xl font-bold text-primary">Ahobilam Rooms</h1>
      <nav className="flex gap-6 text-sm">
        <Link to="/" className="hover:text-primary">Home</Link>
        <Link to="/rooms" className="hover:text-primary">Rooms</Link>
        <Link to="/temple-history" className="hover:text-primary">Temple</Link>
      </nav>
    </div>
  </header>
);

/* ================= FOOTER ================= */
const Footer = () => (
  <footer className="bg-secondary py-10 text-center text-sm text-muted-foreground">
    © {new Date().getFullYear()} Ahobilam Rooms. All rights reserved.
  </footer>
);

/* ================= WHATSAPP BUTTON ================= */
const WhatsAppButton = () => (
  <a
    href="https://wa.me/917675962840"
    target="_blank"
    rel="noopener noreferrer"
    className="fixed bottom-6 right-6 bg-green-500 text-white w-14 h-14 rounded-full flex items-center justify-center text-2xl shadow-lg hover:scale-105 transition"
  >
    💬
  </a>
);

/* ================= FEATURES ================= */
const features = [
  { icon: Wind, title: "Air Conditioned", desc: "All rooms are fully air conditioned" },
  { icon: Star, title: "King Size Beds", desc: "Premium king size beds for comfort" },
  { icon: Wifi, title: "Free Wi-Fi", desc: "High-speed internet" },
  { icon: ShieldCheck, title: "24/7 Security", desc: "Safe & secure stay" },
];

/* ================= MAIN PAGE ================= */
const Index = () => (
  <div className="min-h-screen bg-background">

    <Header />

    {/* HERO */}
    <section className="relative h-[90vh] flex items-center justify-center">
      <img src={heroImage} className="absolute w-full h-full object-cover" />
      <div className="absolute inset-0 bg-black/60" />

      <div className="relative text-center text-white px-4">
        <h1 className="text-4xl md:text-6xl font-bold">
          Ahobilam Rooms
        </h1>
        <p className="mt-3 text-lg">Best stay near Narasimha Temple</p>

        <div className="mt-6 flex gap-4 justify-center">
          <a
            href="https://wa.me/917675962840"
            className="bg-green-500 px-6 py-3 rounded"
          >
            Book Now
          </a>

          <Link to="/rooms" className="border px-6 py-3 rounded">
            View Rooms
          </Link>
        </div>
      </div>
    </section>

    {/* FEATURES */}
    <section className="py-16 container mx-auto px-4">
      <h2 className="text-center text-3xl font-bold mb-10">Facilities</h2>

      <div className="grid grid-cols-2 md:grid-cols-4 gap-6">
        {features.map((f) => (
          <div key={f.title} className="text-center p-4 border rounded">
            <f.icon className="mx-auto text-primary w-8 h-8 mb-2" />
            <h3 className="font-semibold">{f.title}</h3>
            <p className="text-sm text-gray-500">{f.desc}</p>
          </div>
        ))}
      </div>
    </section>

    {/* ROOMS */}
    <section className="py-16 bg-gray-50">
      <h2 className="text-center text-3xl font-bold mb-10">Rooms</h2>

      <div className="grid md:grid-cols-2 gap-8 max-w-4xl mx-auto px-4">
        {[
          { title: "King AC Room - 2 Sharing", guests: "Couples & Pairs" },
          { title: "King AC Room - 3 Sharing", guests: "Family Stay" },
        ].map((room) => (
          <div key={room.title} className="border rounded overflow-hidden">
            <img src={roomImage} className="h-56 w-full object-cover" />

            <div className="p-4">
              <h3 className="font-bold">{room.title}</h3>
              <p className="text-sm text-gray-500">{room.guests}</p>

              <a
                href={`https://wa.me/917675962840?text=I want ${room.title}`}
                className="inline-block mt-3 bg-green-500 text-white px-4 py-2 rounded"
              >
                Book Now
              </a>
            </div>
          </div>
        ))}
      </div>
    </section>

    {/* TEMPLE */}
    <section className="py-16 container mx-auto px-4 grid md:grid-cols-2 gap-8 items-center">
      <div>
        <h2 className="text-3xl font-bold mb-4">Ahobilam Temple</h2>
        <p className="text-gray-600 mb-4">
          Famous Narasimha Swamy temple in Nallamala hills.
        </p>

        <Link to="/temple-history" className="text-primary flex items-center gap-1">
          <MapPin size={16} /> Learn More
        </Link>
      </div>

      <img src={templeImage} className="rounded-lg" />
    </section>

    <Footer />
    <WhatsAppButton />
  </div>
);

export default Index;
