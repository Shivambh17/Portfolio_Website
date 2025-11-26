# Team Photos Directory

## How to Add Team Member Photos

1. **Place your team member photos in this folder** (`portfolio/images/`)

2. **Name your image files** as:
   - `team-member-1.jpg` (or `.png`, `.jpeg`)
   - `team-member-2.jpg`
   - `team-member-3.jpg`
   - `team-member-4.jpg`
   - etc.

3. **Recommended image specifications:**
   - **Format**: JPG, PNG, or JPEG
   - **Size**: 400x400 pixels or larger (square format works best)
   - **File size**: Under 500KB for faster loading
   - **Aspect ratio**: 1:1 (square) is recommended

4. **Update the HTML** (`index.html`) to match your team:
   - Replace "Team Member 1", "Team Member 2", etc. with actual names
   - Update "Role/Position" with actual roles
   - Update the bio descriptions with real information
   - Add or remove team member cards as needed

## Example File Structure:
```
portfolio/
├── images/
│   ├── team-member-1.jpg
│   ├── team-member-2.jpg
│   ├── team-member-3.jpg
│   └── team-member-4.jpg
├── index.html
└── styles.css
```

## Adding More Team Members

To add more team members, copy one of the team member card sections in `index.html` and update:
- The image source path
- The name
- The role
- The bio

The grid will automatically adjust to show all team members.

## Placeholder Image

If an image is missing, the website will try to load `placeholder.jpg`. You can add a placeholder image with this name if desired.

