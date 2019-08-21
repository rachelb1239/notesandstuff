# SASS 
-Date 7/21/2019

# LINKS/RESOURCES
- Homepage: https://sass-lang.com/
- Install: https://sass-lang.com/install
- Overqualified CSS: https://github.com/CSSLint/csslint/wiki/Disallow-overqualified-elements

# DESCRIPTION
- CSS extension language
- Write in SASS OR SCSS, compile to single CSS file

# BASICS
 - Preprocessing: bundle all your files into a single css file
 - Variables: store info you want to reuse throughout style sheet (fonts, colors, etc)
 - Nesting: nest selectors for visibility
    - DON'T OVER-DO NESTING - will lead to overqualified CSS (redundant, unecessary selectors - see link)
 - Partials: allow for snippets to include in other files, but not as part of bundled file
 - Import: Import during preprossing instead of making new http requests on each import statement
 - Mixins: group CSS declarations for reuse throughout site 
    - useful for handling differences in syntax between versions/venders
 - Extend/Inheritance: pass css properties from one selector to another 
    - Think classes e.g. class fork extends silverware (not actual syntax)
 - Operators: do math
    - Convert pixels to percentages