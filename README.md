# The Cellular Masquerade

An interactive educational visualization demonstrating the dot product's role in cellular biology and population dynamics.

## Overview

This project presents an elegant web-based visualization that reveals how linear algebra, specifically the dot product operation, serves as a fundamental tool in understanding cellular reproduction, gene expression, and population modeling. Through an interactive simulator, users can explore how mathematical vectors represent biological states and uncover hidden patterns in the cell cycle.

## Features

### Interactive Gene Expression Simulator
- Real-time dot product calculations based on user-controlled gene expression levels
- Visual feedback showing cell cycle phase transitions
- Four key genes involved in cell division:
  - CDK1 Expression
  - Cyclin B Expression
  - Topoisomerase Expression
  - Aurora Kinase Expression

### Educational Content
The visualization demonstrates three core applications of the dot product in biology:

1. **Cell Cycle Similarity**: Compare gene expression vectors to determine where a cell is in the reproductive cycle
2. **Population Dynamics**: Leslie Matrix modeling using dot products to calculate generational transitions
3. **Geometric Projection**: Analyzing cell fate by projecting developmental trajectories onto division axes

### Visual Design
- Dark, sophisticated theme with ornamental borders
- Responsive design that adapts to mobile, tablet, and desktop screens
- Smooth animations and transitions
- Color-coded cell phase indicators:
  - G0 Phase (Resting) - Brown tones
  - G1/G2 Phase (Preparing) - Teal tones
  - S Phase (DNA Replication) - Gold tones
  - M Phase (Mitosis) - Red tones

## Usage

### Running the Application

Simply open `index.html` in a modern web browser. No server or build process required.

### Interacting with the Simulator

1. Adjust the gene expression sliders to modify the cellular state vector
2. Watch the dot product calculation update in real-time
3. Observe the cell circle change color and phase label based on similarity to the reference metaphase state
4. Monitor the similarity percentage to see how closely your cell matches the division-ready state

### Target Reference Vector

The simulator uses a reference vector representing ideal Metaphase state:
```
R = [5.0, 5.0, 4.0, 5.0]
```

Match all gene expression levels to these targets to achieve maximum similarity and trigger the Mitosis phase.

## Mathematical Concepts

### Dot Product Calculation
```
R · U = Σ(r_i × u_i)
```

### Cosine Similarity
The visualization uses cosine similarity to normalize the comparison:
```
similarity = (R · U) / (|R| × |U|)
```

This provides a scale-invariant measure of similarity between 0 and 1.

### Phase Classification
- **> 85% similarity**: M-Phase (Mitosis)
- **60-85% similarity**: S-Phase (DNA Replication)
- **30-60% similarity**: G1/G2 Phase (Preparing)
- **< 30% similarity**: G0 Phase (Resting)

## Technical Details

### Technologies Used
- Pure HTML5
- CSS3 with advanced features:
  - CSS Grid for responsive layouts
  - Gradients and shadows for visual depth
  - Media queries for mobile responsiveness
  - Touch device optimizations
- Vanilla JavaScript (no frameworks required)

### Browser Compatibility
Works on all modern browsers supporting:
- HTML5
- CSS3 Grid
- ES6 JavaScript

### Responsive Breakpoints
- Small Mobile: 360px - 575px
- Medium Mobile/Landscape: 576px - 767px
- Tablets: 768px - 991px
- Large Tablets/Small Laptops: 992px - 1199px
- Desktop: 1200px+

## Educational Applications

This visualization is suitable for:
- **Bioinformatics courses**: Demonstrating gene expression analysis
- **Linear algebra classes**: Real-world applications of dot products
- **Cell biology education**: Understanding the cell cycle phases
- **Population dynamics**: Introduction to Leslie Matrix models
- **Data science**: Vector space representations of biological data

## File Structure

```
dot-product-cell-cycle/
├── index.html          # Main application file (standalone)
└── README.md          # This file
```

## Customization

### Modifying the Reference Vector
Edit line 1289 in `index.html`:
```javascript
const R = [5.0, 5.0, 4.0, 5.0];
```

### Adjusting Phase Thresholds
Modify the conditional statements starting at line 1332 to change when phases transition.

### Styling
All styles are contained in the `<style>` section (lines 7-1149). Modify CSS variables or specific selectors to customize appearance.

## License

This is an educational resource. Feel free to use and adapt for educational purposes.

## Author

An illuminated chamber where linear algebra removes the veil from life itself.
