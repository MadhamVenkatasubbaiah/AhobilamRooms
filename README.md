import React from "react";

export default function App() {
  const phone = "917675962840";

  return (
    <div style={styles.page}>

      {/* HEADER */}
      <header style={styles.header}>
        <h2 style={styles.logo}>Ahobilam Haven Stay</h2>
        <a style={styles.bookBtn} href={`https://wa.me/${phone}`} target="_blank">
          Book Now
        </a>
      </header>

      {/* HERO */}
      <section style={styles.hero}>
        <div style={styles.overlay}></div>

        <div style={styles.heroContent}>
          <h1 style={styles.title}>Peaceful Stay Near Ahobilam Temple</h1>
          <p>Comfortable rooms • Family friendly • Near Narasimha Temple</p>

          <a
            href={`https://wa.me/${phone}`}
            style={styles.greenBtn}
            target="_blank"
          >
            Book on WhatsApp
          </a>
        </div>
      </section>

      {/* FEATURES */}
      <section style={styles.section}>
        <h2>Why Choose Us</h2>

        <div style={styles.grid}>
          <div style={styles.card}>🛏 Clean Rooms</div>
          <div style={styles.card}>❄ AC Available</div>
          <div style={styles.card}>🔒 Safe Stay</div>
          <div style={styles.card}>📍 Near Temple</div>
        </div>
      </section>

      {/* ROOMS */}
      <section style={styles.sectionAlt}>
        <h2>Our Rooms</h2>

        <div style={styles.grid}>

          <div style={styles.roomCard}>
            <img
              src="https://images.unsplash.com/photo-1560184897-ae75f418493e"
              style={styles.roomImg}
            />
            <h3>2 Sharing AC Room</h3>
            <a style={styles.greenBtn} href={`https://wa.me/${phone}`}>
              Book Now
            </a>
          </div>

          <div style={styles.roomCard}>
            <img
              src="https://images.unsplash.com/photo-1578683010236-d716f9a3f461"
              style={styles.roomImg}
            />
            <h3>Family AC Room</h3>
            <a style={styles.greenBtn} href={`https://wa.me/${phone}`}>
              Book Now
            </a>
          </div>

        </div>
      </section>

      {/* ABOUT TEMPLE */}
      <section style={styles.about}>
        <div>
          <h2>Ahobilam Temple</h2>
          <p>
            One of the most powerful Narasimha Swamy temples in India,
            located in the Nallamala Hills of Andhra Pradesh.
          </p>
        </div>

        <img
          src="https://images.unsplash.com/photo-1601404395112-9e5a6a7b6c56"
          style={styles.templeImg}
        />
      </section>

      {/* FOOTER */}
      <footer style={styles.footer}>
        © {new Date().getFullYear()} Ahobilam Haven Stay
      </footer>

      {/* FLOAT WHATSAPP */}
      <a
        href={`https://wa.me/${phone}`}
        target="_blank"
        style={styles.whatsapp}
      >
        💬
      </a>

    </div>
  );
}

/* ================= STYLES ================= */
const styles: any = {

  page: {
    fontFamily: "Arial",
    margin: 0,
    padding: 0
  },

  header: {
    position: "fixed",
    top: 0,
    width: "100%",
    background: "#ff9933",
    display: "flex",
    justifyContent: "space-between",
    padding: "15px 20px",
    alignItems: "center",
    zIndex: 1000
  },

  logo: {
    color: "white",
    margin: 0
  },

  bookBtn: {
    background: "#25D366",
    color: "white",
    padding: "8px 14px",
    borderRadius: "5px",
    textDecoration: "none"
  },

  hero: {
    height: "90vh",
    backgroundImage: "url('https://images.unsplash.com/photo-1542314831-068cd1dbfeeb')",
    backgroundSize: "cover",
    backgroundPosition: "center",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    color: "white",
    position: "relative",
    marginTop: "70px"
  },

  overlay: {
    position: "absolute",
    width: "100%",
    height: "100%",
    background: "rgba(0,0,0,0.6)"
  },

  heroContent: {
    position: "relative",
    textAlign: "center"
  },

  title: {
    fontSize: "42px"
  },

  section: {
    padding: "60px",
    textAlign: "center"
  },

  sectionAlt: {
    padding: "60px",
    background: "#f7f7f7",
    textAlign: "center"
  },

  grid: {
    display: "flex",
    gap: "20px",
    justifyContent: "center",
    flexWrap: "wrap",
    marginTop: "20px"
  },

  card: {
    padding: "20px",
    background: "white",
    borderRadius: "10px",
    width: "150px"
  },

  roomCard: {
    width: "250px",
    background: "white",
    borderRadius: "10px",
    padding: "10px"
  },

  roomImg: {
    width: "100%",
    height: "180px",
    objectFit: "cover",
    borderRadius: "10px"
  },

  about: {
    display: "flex",
    gap: "20px",
    padding: "60px",
    alignItems: "center",
    flexWrap: "wrap"
  },

  templeImg: {
    width: "350px",
    borderRadius: "10px"
  },

  footer: {
    background: "#222",
    color: "white",
    textAlign: "center",
    padding: "20px"
  },

  whatsapp: {
    position: "fixed",
    bottom: "20px",
    right: "20px",
    width: "60px",
    height: "60px",
    background: "#25D366",
    color: "white",
    borderRadius: "50%",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    fontSize: "28px",
    textDecoration: "none"
  }
};
