# 🏠 3D House Survey - Interactive Home Profile

An interactive 3D web application that creates a personalized digital representation of your home as you complete a comprehensive home survey. Built with Three.js, this gamified survey experience visualizes your home in real-time, updating the 3D model based on your responses.

## ✨ Features

### Interactive 3D Home Visualization
- **Dynamic House Building**: Watch your 3D house evolve with each survey question you answer
- **Realistic Materials & Textures**: Wood, metal, glass, and fabric materials render with high fidelity
- **Progressive Construction**: House builds progressively from exterior to interior as you advance through survey sections
- **Multiple Camera Views**: Switch between overview, interior, and room-specific views (bedroom, bathroom, kitchen, living room, terrace, top view)

### Comprehensive Home Survey
The application contains **15 interactive questions** covering:

#### Home Structure (Questions 1-4)
- 🏠 **Dwelling Type**: Single family home, apartment, townhouse, or condominium
- 🔑 **Ownership**: Own or rent
- 📏 **Living Area**: Home size in square feet
- 🛏️ **Bedrooms**: Number of bedrooms (1, 2, 3, 4+)

#### Occupancy & Systems (Questions 5-9)
- 👥 **Occupants**: Number of people living in the home
- 🔥 **Heating System**: Central furnace, heat pump, baseboard heater, or none
- ❄️ **Cooling System**: Central AC, evaporative cooling, or none
- 💧 **Water Heater**: Electric, gas, or none
- 🌡️ **Smart Thermostat**: Yes or no

#### Appliances & Features (Questions 10-15)
- 🍳 **Kitchen**: Electric/gas stove, electric/gas oven, refrigerator
- 🧺 **Laundry**: Washing machine, dryer, dishwasher
- ☀️ **Solar Panels**: Yes or no
- 🚗 **Electric Vehicle**: Yes or no (with EV charger visualization)
- 🏊 **Swimming Pool**: Yes or no
- 📺 **Entertainment**: Television, computer, game console

### Gamification Elements
- **Progress Bar**: Visual indication of survey completion (Q1 of 15, etc.)
- **Room Labels**: Emoji-enhanced labels showing which room/system you're surveying
- **Completion Screen**: Celebratory summary upon finishing all questions
- **House Tour**: Option to view your completed 3D home with a camera tour
- **Restart Option**: Ability to start over and redesign your home

### Advanced 3D Features
- **3D Appliances**: Rendered models for water heaters, thermostats, solar panels, EV chargers, pools, etc.
- **Interior Furnishings**: Beds, furniture, and room-specific decorations
- **Environmental Elements**: Stars, moon, ground, trees, bushes, fence, mailbox, neighbor silhouettes
- **Lighting System**: Directional sunlight with shadows and dynamic ambient lighting
- **Responsive Design**: Scales to different window sizes with appropriate camera adjustments

## 🛠️ Technical Stack

- **3D Rendering**: Three.js library for WebGL 3D graphics
- **Canvas Textures**: Procedurally generated wood, metal, and fabric textures
- **Materials**: PBR (Physically Based Rendering) materials with metalness and roughness properties
- **Performance Optimization**: Global scaling and shadow mapping for efficient rendering
- **Responsive Layout**: Flex-based CSS with mobile and desktop support

## 🎮 How to Use

1. **Open the Application**: Load the HTML file in a modern web browser
2. **Answer Questions**: Select answers or enter values for each survey question
3. **Watch Your Home Build**: See your 3D house evolve in real-time as you progress
4. **Explore Different Views**: Use the camera control buttons to view different areas:
   - **Overview**: Exterior view of the entire house
   - **Inside**: Interior perspective
   - **Room Views**: Specific views for bedroom, bathroom, kitchen, living room, terrace
   - **Top View**: Bird's-eye perspective
5. **Complete the Survey**: Finish all 15 questions to see your completion screen
6. **House Tour**: Click "House Tour" to see an animated camera tour of your custom home
7. **Start Over**: Redesign your home with different choices

## 🏗️ Project Structure

### HTML Components
- **Loading Overlay**: Initial loading screen during scene initialization
- **Camera Controls**: Navigation buttons for different views
- **Room Label**: Displays current section being surveyed with emoji
- **Survey Panel**: Left sidebar containing questions and progress bar
- **Completion Screen**: Modal shown upon survey completion with badges

### JavaScript Sections
- **Survey State Management**: Tracks user answers and home configuration
- **3D Scene Setup**: Three.js initialization, lighting, and camera management
- **House Building**: Dynamic generation of rooms, walls, doors, windows, roof
- **Appliance Creation**: Functions for rendering each home appliance and feature
- **Room Layouts**: Customizable bedroom, bathroom, kitchen, and living area layouts
- **Camera Control**: Multiple preset camera positions for different views
- **Animation Loop**: Continuous rendering and scene updates

### CSS Styling
- **Survey Panel**: Sidebar styling with progress bar and questions
- **Camera Controls**: Button layout for view selection
- **Completion Screen**: Modal overlay with celebration design
- **Responsive Grid**: Mobile-first layout with desktop breakpoints

## 📊 Data Mapping

Survey answers map to home profile attributes:
- Questions are tagged with IDs (Q1-Q15)
- Each answer includes descriptive text, icons, and state mapper values
- State mappers follow `HP:attribute:value` pattern for home properties
- Appliance markers follow `AP:id:property:value` pattern

## 🎨 Customization

### Adding New Questions
New survey questions can be added to the `surveyQuestions` array with:
- Unique ID (Q16, Q17, etc.)
- Question text and description
- Answer choices with icons and descriptions
- State mapper for tracking responses
- Room label with emoji

### Modifying House Appearance
- **Materials**: Edit the `SharedMaterials` object to change colors and surface properties
- **House Dimensions**: Adjust `livingArea` and `floors` calculations in construction functions
- **Appliance Placement**: Modify coordinates in `createXXX()` functions

### Changing Colors & Themes
- Background color: Edit `scene.background` in `initScene()`
- Lighting: Modify `sunLight` properties and ambient light intensity
- Material colors: Update color hex values in material definitions

## 🌐 Browser Compatibility

- Requires WebGL support
- Tested on modern browsers (Chrome, Firefox, Safari, Edge)
- Responsive design works on desktop and tablet screens

## 📝 Version

**v2.2-FIXED** - Latest stable release with grid-based floor planning and updated UI layout

## 🚀 Future Enhancements

Potential improvements:
- GLTF model loading for more realistic appliances
- Multi-floor house layout variations
- Energy efficiency scoring based on appliances
- Export home profile as PDF or 3D file
- Multiplayer home sharing
- Mobile app optimization
- VR/360° house tour mode

## 📄 License

Check project root for license information.

---

**Built with ❤️ using Three.js for interactive home profiling**
