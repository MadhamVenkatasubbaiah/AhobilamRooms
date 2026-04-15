import React from "react";

export default function App() {

  const phone = "917675962840";

  return (
    <div style={styles.page}>

      {/* ================= HEADER ================= */}
      <header style={styles.header}>
        <h1 style={styles.logo}>AHOBILAM ROOMS</h1>
      </header>

      {/* ================= HERO ================= */}
      <section style={styles.hero}>
        <div style={styles.overlay}></div>

        <div style={styles.heroContent}>
          <h1 style={styles.title}>Ahobilam Rooms</h1>
          <p>Best stay near Narasimha Temple</p>

          <a
            style={styles.btnGreen}
            href={`https://wa.me/${phone}`}
            target="_blank"
          >
            Book Now
          </a>
        </div>
      </section>

      {/* ================= ROOMS ================= */}
      <section style={styles.section}>
        <h2>Rooms</h2>

        <div style={styles.cardContainer}>

          <div style={styles.card}>
            <img
              src="https://images.unsplash.com/photo-1560184897-ae75f418493e"
              style={styles.image}
            />
            <h3>King AC Room</h3>
            <a
              style={styles.btnGreen}
              href={`https://wa.me/${phone}?text=I want King AC Room`}
              target="_blank"
            >
              Book
            </a>
          </div>

          <div style={styles.card}>
            <img
              src="https://images.unsplash.com/photo-1578683010236-d716f9a3f461"
              style={styles.image}
            />
            <h3>Family Room</h3>
            <a
              style={styles.btnGreen}
              href={`https://wa.me/${phone}?text=I want Family Room`}
              target="_blank"
            >
              Book
            </a>
          </div>

        </div>
      </section>

      {/* ================= TEMPLE ================= */}
      <section style={styles.sectionRow}>
        <img
          src="https://images.unsplash.com/photo-1601404395112-9e5a6a7b6c56"
          style={styles.templeImg}
        />

        <div>
          <h2>Ahobilam Temple</h2>
          <p>
            Famous Narasimha Swamy temple in Andhra Pradesh. Divine and peaceful place.
          </p>
        </div>
      </section>

      {/* ================= FOOTER ================= */}
      <footer style={styles.footer}>
        © {new Date().getFullYear()} Ahobilam Rooms
      </footer>

      {/* ================= WHATSAPP FLOAT ================= */}
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

/* ================= INLINE STYLES ================= */
const styles: any = {

  page: {
    fontFamily: "Arial",
    margin: 0,
    padding: 0,
    overflowX: "hidden"
  },

  header: {
    position: "fixed",
    top: 0,
    left: 0,
    width: "100%",
    height: "70px",
    background: "#FF9933",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    zIndex: 1000,
    color: "white"
  },

  logo: {
    margin: 0,
    fontSize: "22px"
  },

  hero: {
    height: "90vh",
    backgroundImage: "url('https://images.unsplash.com/photo-1542314831-068cd1dbfeeb')",
    backgroundSize: "cover",
    backgroundPosition: "center",
    position: "relative",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    color: "white",
    marginTop: "70px"
  },

  overlay: {
    position: "absolute",
    top: 0,
    left: 0,
    width: "100%",
    height: "100%",
    background: "rgba(0,0,0,0.6)"
  },

  heroContent: {
    position: "relative",
    textAlign: "center"
  },

  title: {
    fontSize: "40px",
    marginBottom: "10px"
  },

  section: {
    padding: "50px",
    textAlign: "center"
  },

  cardContainer: {
    display: "flex",
    gap: "20px",
    justifyContent: "center",
    flexWrap: "wrap"
  },

  card: {
    width: "280px",
    border: "1px solid #ddd",
    borderRadius: "10px",
    padding: "15px"
  },

  image: {
    width: "100%",
    height: "180px",
    objectFit: "cover",
    borderRadius: "10px"
  },

  sectionRow: {
    display: "flex",
    gap: "20px",
    padding: "50px",
    alignItems: "center",
    flexWrap: "wrap"
  },

  templeImg: {
    width: "400px",
    maxWidth: "100%",
    borderRadius: "10px"
  },

  btnGreen: {
    display: "inline-block",
    marginTop: "10px",
    background: "#25D366",
    color: "white",
    padding: "10px 15px",
    borderRadius: "5px",
    textDecoration: "none"
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
    fontSize: "28px",
    borderRadius: "50%",
    display: "flex",
    alignItems: "center",
    justifyContent: "center",
    textDecoration: "none"
  }
};
