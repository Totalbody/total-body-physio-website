import React from 'react';

const HomePage = () => {
  // Updated color scheme to match the logo
  const colors = {
    darkGreen: '#036F39',  // Dark green from the logo
    lightGreen: '#8DC63F', // Light green from the logo
    white: '#FFFFFF',
    black: '#000000',
  };

  // Styles
  const styles = {
    fontFamily: "'Roboto', 'Helvetica', 'Arial', sans-serif",
    button: {
      backgroundColor: colors.darkGreen,
      color: colors.white,
      padding: '0.75rem 1.5rem',
      border: 'none',
      borderRadius: '5px',
      fontSize: '1rem',
      fontWeight: '500',
      cursor: 'pointer',
      transition: 'all 0.3s ease',
      textTransform: 'uppercase',
      letterSpacing: '1px',
    },
    section: {
      padding: '5rem 2rem',
    },
    container: {
      maxWidth: '1200px',
      margin: '0 auto',
    },
  };

  return (
    <div style={{ ...styles, color: colors.darkGreen }}>
      {/* Header with Actual Logo */}
      <header style={{ backgroundColor: colors.white, padding: '1rem', boxShadow: '0 2px 10px rgba(0,0,0,0.1)' }}>
        <div style={{ ...styles.container, display: 'flex', justifyContent: 'space-between', alignItems: 'center' }}>
          <img 
            src="/path/to/total-body-physio-logo.png" 
            alt="Total Body Physio Logo" 
            style={{ height: '60px', width: 'auto' }} 
          />
          <nav>
            <ul style={{ display: 'flex', gap: '2rem', listStyle: 'none' }}>
              {['Services', 'Locations', 'About Us', 'Contact'].map((item) => (
                <li key={item}>
                  <a href={`#${item.toLowerCase().replace(' ', '-')}`} 
                     style={{ color: colors.darkGreen, textDecoration: 'none', transition: 'color 0.3s', fontWeight: '500' }}
                     onMouseEnter={(e) => e.target.style.color = colors.lightGreen}
                     onMouseLeave={(e) => e.target.style.color = colors.darkGreen}>
                    {item}
                  </a>
                </li>
              ))}
            </ul>
          </nav>
        </div>
      </header>

      {/* Hero Section */}
      <section style={{ 
        ...styles.section, 
        backgroundImage: 'url("/api/placeholder/1600/900")', 
        backgroundSize: 'cover',
        backgroundPosition: 'center',
        color: colors.white,
        textAlign: 'center',
        position: 'relative',
      }}>
        <div style={{ backgroundColor: 'rgba(0,0,0,0.6)', position: 'absolute', top: 0, left: 0, right: 0, bottom: 0 }} />
        <div style={{ ...styles.container, position: 'relative', zIndex: 1 }}>
          <h1 style={{ fontSize: '3.5rem', marginBottom: '1rem', fontWeight: '700' }}>Expert Physiotherapy for Total Body Wellness</h1>
          <p style={{ fontSize: '1.5rem', marginBottom: '2rem', maxWidth: '800px', margin: '0 auto 2rem' }}>Personalised care to help you move, feel, and live better</p>
          <button style={styles.button} onMouseEnter={(e) => e.target.style.backgroundColor = colors.lightGreen} onMouseLeave={(e) => e.target.style.backgroundColor = colors.darkGreen}>
            Book an Appointment
          </button>
        </div>
      </section>

      {/* Services Overview */}
      <section id="services" style={{ ...styles.section, backgroundColor: colors.white }}>
        <div style={styles.container}>
          <h2 style={{ fontSize: '2.5rem', textAlign: 'center', marginBottom: '3rem', color: colors.darkGreen }}>Our Services</h2>
          <div style={{ display: 'flex', justifyContent: 'space-around', flexWrap: 'wrap', gap: '2rem' }}>
            {['Sports Injury Rehabilitation', 'Manual Therapy', 'Postural Correction'].map((service) => (
              <div key={service} style={{ backgroundColor: colors.white, padding: '2rem', borderRadius: '10px', boxShadow: '0 4px 20px rgba(0,0,0,0.1)', textAlign: 'center', maxWidth: '300px' }}>
                <img src="/api/placeholder/80/80" alt={service} style={{ marginBottom: '1.5rem' }} />
                <h3 style={{ fontSize: '1.5rem', marginBottom: '1rem', color: colors.darkGreen }}>{service}</h3>
                <p style={{ color: colors.darkGreen }}>Specialised treatment to address your specific needs and goals.</p>
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* About Us */}
      <section id="about" style={{ ...styles.section, backgroundColor: colors.lightGreen, color: colors.white }}>
        <div style={{ ...styles.container, display: 'flex', alignItems: 'center', gap: '4rem', flexWrap: 'wrap' }}>
          <div style={{ flex: 1, minWidth: '300px' }}>
            <h2 style={{ fontSize: '2.5rem', marginBottom: '1.5rem', fontWeight: '700' }}>About Total Body Physio</h2>
            <p style={{ marginBottom: '1rem', fontSize: '1.1rem', lineHeight: '1.6' }}>
              At Total Body Physio, we're committed to providing comprehensive, personalised physiotherapy care. 
              Our team of expert therapists uses evidence-based techniques to help you achieve optimal health and wellness.
            </p>
            <p style={{ fontSize: '1.1rem', lineHeight: '1.6' }}>
              Whether you're recovering from an injury, managing chronic pain, or looking to improve your overall physical condition, 
              we're here to support you every step of the way.
            </p>
          </div>
          <div style={{ flex: 1, minWidth: '300px' }}>
            <img src="/api/placeholder/600/400" alt="Our Team" style={{ width: '100%', borderRadius: '10px', boxShadow: '0 4px 20px rgba(0,0,0,0.3)' }} />
          </div>
        </div>
      </section>

      {/* Call-to-Action */}
      <section style={{ ...styles.section, backgroundColor: colors.darkGreen, color: colors.white, textAlign: 'center' }}>
        <div style={styles.container}>
          <h2 style={{ fontSize: '2.5rem', marginBottom: '1.5rem' }}>Ready to Start Your Journey to Better Health?</h2>
          <button style={{ ...styles.button, backgroundColor: colors.white, color: colors.darkGreen }} 
                  onMouseEnter={(e) => { e.target.style.backgroundColor = colors.lightGreen; e.target.style.color = colors.white; }}
                  onMouseLeave={(e) => { e.target.style.backgroundColor = colors.white; e.target.style.color = colors.darkGreen; }}>
            Book an Appointment
          </button>
        </div>
      </section>

      {/* Footer */}
      <footer style={{ backgroundColor: colors.black, color: colors.white, padding: '3rem 1rem', textAlign: 'center' }}>
        <div style={styles.container}>
          <p style={{ fontSize: '1.1rem' }}>&copy; 2024 Total Body Physio. All rights reserved.</p>
        </div>
      </footer>
    </div>
  );
};

export default HomePage;
