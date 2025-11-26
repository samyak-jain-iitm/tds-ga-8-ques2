---
marp: true
theme: gaia
paginate: true
author: Technical Writer
title: API Documentation V2.0
backgroundColor: #fff
---

<style>
/* Customizing the theme colors */
:root {
  --color-foreground: #333;
  --color-background: #fff;
  --color-highlight: #d9453a;
}
section {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.5rem;
}
h1, h2 {
  color: #2c3e50;
}
/* Style for the footer specifically */
footer {
  color: #7f8c8d;
}
</style>

# API Product Documentation
## Version 2.0 Release Notes

**Contact:** [25ds1000058@ds.study.iitm.ac.in](mailto:25ds1000058@ds.study.iitm.ac.in)

---

![bg right:40%](https://images.unsplash.com/photo-1558494949-ef2bb6db8744?auto=format&fit=crop&w=800&q=80)

# System Architecture

The new architecture relies on microservices to ensure high availability.

- **Scalability:** Horizontal scaling supported
- **Reliability:** 99.99% Uptime SLA
- **Security:** OAuth2 implementation

*See the diagram on the right for the data flow.*

---

# Algorithmic Efficiency

To improve response times, we optimized the search algorithm.

### Complexity Analysis
We reduced the time complexity from quadratic to log-linear:

$$
T(n) = 2T\left(\frac{n}{2}\right) + O(n) \Rightarrow O(n \log n)
$$

### Probability Formula
Success rate calculation:

The probability of collision is defined as $P(A) \approx 1 - e^{-\frac{n^2}{2d}}$.

---

# Internal Roadmap

This slide uses custom directives to change the background color and add a header.

1. **Q1:** Beta testing with stakeholders
2. **Q2:** Public API release
3. **Q3:** Deprecation of V1.0 endpoints

```javascript
// Deprecation Warning Example
console.warn("Endpoint /v1/auth is deprecated. Use /v2/auth.");
