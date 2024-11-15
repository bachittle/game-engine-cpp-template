# Design Philosophy

## Core Philosophy: Maximum Impact, Minimal Code

This template follows a "maximum impact, minimal code" philosophy, specifically designed for:
- Indie developers building game engines from scratch
- Developers learning C++ and graphics programming
- Projects requiring minimal context (like AI/ML applications)
- Rapid prototyping and proof-of-concept development

The focus is on getting core features working quickly, letting developers concentrate on their game's unique aspects rather than engine complexity. 
By using Modern OpenGL, we hit a sweet spot between power and simplicity - more capable than legacy OpenGL but without Vulkan's steep learning curve.

## Example-Driven Development

Rather than hiding functionality behind layers of abstraction, this template embraces direct interaction with the underlying libraries. 
Look at `example.cpp` - it's not wrapped in classes or complex hierarchies. Instead, it shows exactly how to:
- Initialize GLFW and OpenGL
- Set up ImGui
- Create a basic render loop

This approach has several benefits:
- Learn by doing - see exactly how things work
- Modify anything easily - no need to understand complex abstractions
- Keep code searchable and debuggable
- Maintain small context size for AI/ML applications

## Technology Choices

### Modern OpenGL
- Powerful enough for serious 3D development
- Simpler than Vulkan/DirectX while still being modern
- Excellent documentation and community support
- Good balance of performance and accessibility

### GLFW
- Minimal window and OpenGL context creation
- Cross-platform with consistent API
- Just enough functionality without bloat

### Dear ImGui
- Immediate mode UI perfect for rapid development
- Minimal dependencies compared to alternatives like Qt
- Examples-based learning approach matches our philosophy
- Great for debug interfaces and tools

## Intentionally Minimal Feature Set

We deliberately exclude many features you might find in other engines:
- No audio system
- No input handling beyond basic GLFW
- No physics engine
- No scene graph
- No asset management system

This is not an oversight - it's a design choice. Benefits include:
- Smaller learning curve
- Less code to maintain
- Clearer understanding of each component
- Freedom to add only what you need
- Avoid feature creep

## When to Use This Template

Perfect for:
- Learning graphics programming
- Prototyping game ideas
- Starting fresh game projects
- AI/ML projects needing graphics
- Small indie games

Consider alternatives when:
- You need many engine features out of the box
- Maximum performance is critical (consider Vulkan)
- You have a large team needing structured engine architecture
- You need rapid commercial game development

## Future Considerations

While maintaining our minimal philosophy, we might carefully consider:
- Optional Vulkan template for performance-critical projects
- Example-based additions for common features (audio, input, etc.)
- Additional learning resources and documentation

However, any additions will follow our core principles:
- Keep it example-driven
- Maintain direct library access
- Avoid unnecessary abstraction
- Prevent feature creep

Remember: This template's strength is in what it doesn't do as much as what it does. It provides a foundation for understanding and building, rather than a black box of functionality.