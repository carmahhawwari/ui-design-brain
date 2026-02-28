# UI Component Reference

Complete reference for 60 UI components with best practices, common layouts, and aliases.
Sourced from [component.gallery](https://component.gallery) and enriched with production-grade guidance.

---

## Contents

- [Accordion](#accordion)
- [Alert](#alert)
- [Avatar](#avatar)
- [Badge](#badge)
- [Breadcrumbs](#breadcrumbs)
- [Button](#button)
- [Button group](#button-group)
- [Card](#card)
- [Carousel](#carousel)
- [Checkbox](#checkbox)
- [Color picker](#color-picker)
- [Combobox](#combobox)
- [Date input](#date-input)
- [Datepicker](#datepicker)
- [Drawer](#drawer)
- [Dropdown menu](#dropdown-menu)
- [Empty state](#empty-state)
- [Fieldset](#fieldset)
- [File](#file)
- [File upload](#file-upload)
- [Footer](#footer)
- [Form](#form)
- [Header](#header)
- [Heading](#heading)
- [Hero](#hero)
- [Icon](#icon)
- [Image](#image)
- [Label](#label)
- [Link](#link)
- [List](#list)
- [Modal](#modal)
- [Navigation](#navigation)
- [Pagination](#pagination)
- [Popover](#popover)
- [Progress bar](#progress-bar)
- [Progress indicator](#progress-indicator)
- [Quote](#quote)
- [Radio button](#radio-button)
- [Rating](#rating)
- [Rich text editor](#rich-text-editor)
- [Search input](#search-input)
- [Segmented control](#segmented-control)
- [Select](#select)
- [Separator](#separator)
- [Skeleton](#skeleton)
- [Skip link](#skip-link)
- [Slider](#slider)
- [Spinner](#spinner)
- [Stack](#stack)
- [Stepper](#stepper)
- [Table](#table)
- [Tabs](#tabs)
- [Text input](#text-input)
- [Textarea](#textarea)
- [Toast](#toast)
- [Toggle](#toggle)
- [Tooltip](#tooltip)
- [Tree view](#tree-view)
- [Video](#video)
- [Visually hidden](#visually-hidden)

---

## Accordion

**Also known as:** Arrow toggle  ·  Collapse  ·  Collapsible sections  ·  Collapsible  ·  Details  ·  Disclosure  ·  Expandable  ·  Expander

An accordion is a vertical stack of interactive headings used to toggle the display of further information; each item can be 'collapsed' with just a short label visible or 'expanded' to show the full content.

**Best practices:**
- Use for long-form content that benefits from progressive disclosure
- Keep headings concise and scannable — they are the primary navigation
- Allow multiple sections open simultaneously unless space is critically limited
- Include a subtle expand/collapse icon (chevron) aligned consistently on the right
- Animate open/close with a short ease-out transition (150–250 ms)
- Ensure keyboard navigation: Enter/Space toggles, arrow keys move between headers

**Common layouts:**
- FAQ page with stacked question/answer pairs
- Settings panel with grouped preference sections
- Sidebar filter groups in e-commerce or dashboards
- Mobile navigation with expandable menu sections

---

## Alert

**Also known as:** Notification  ·  Feedback  ·  Message  ·  Banner  ·  Callout

A way of informing the user of important changes in a prominent way.

**Best practices:**
- Use semantic color coding: red for errors, amber for warnings, green for success, blue for info
- Include a clear, actionable message — not just a status label
- Provide a dismiss action for non-critical alerts
- Position inline alerts close to the relevant content, not floating arbitrarily
- Use an icon alongside color to ensure accessibility for color-blind users
- Keep alert text to one or two sentences maximum

**Common layouts:**
- Top-of-page banner for system-wide announcements
- Inline form validation message beneath an input field
- Toast notification stack in the bottom-right corner
- Contextual warning inside a card or settings section

---

## Avatar

A graphical representation of a user: usually a photo, illustration, or initial.

**Best practices:**
- Support three sizes: small (24–32 px), medium (40–48 px), large (64–80 px)
- Fall back gracefully: image → initials → generic icon
- Use a subtle ring or border to separate the avatar from its background
- For groups, stack avatars with a slight overlap and a '+N' overflow indicator
- Ensure the image is loaded lazily with a placeholder shimmer

**Common layouts:**
- User profile header with name and role
- Comment thread with avatar beside each message
- Team member list with stacked avatar group
- Navigation bar user menu trigger

---

## Badge

**Also known as:** Tag  ·  Label  ·  Chip

A small label, generally appearing inside or in close proximity to another larger interface component, representing a status, property, or some other metadata.

**Best practices:**
- Keep badge text to one or two words — they are labels, not sentences
- Use a limited palette of badge colors mapped to clear semantics
- Ensure sufficient contrast between badge text and background (WCAG AA minimum)
- Use pill shape (fully rounded corners) for status badges, rounded rectangles for tags
- Avoid overusing badges — if everything is badged, nothing stands out

**Common layouts:**
- Status indicator on a table row (Active, Pending, Archived)
- Tag cloud beneath a blog post or product card
- Notification count on a nav icon
- Feature label on a pricing tier card

---

## Breadcrumbs

**Also known as:** Breadcrumb trail

A list of links showing the location of the current page in the navigational hierarchy.

**Best practices:**
- Show the full hierarchy path; truncate middle segments on mobile with an ellipsis menu
- The current page should be the last item and should not be a link
- Use a subtle separator (/ or ›) with adequate spacing
- Place breadcrumbs near the top of the content area, below the header
- Keep breadcrumb text lowercase or sentence-case for readability

**Common layouts:**
- E-commerce category → subcategory → product page
- Documentation site section navigation
- Dashboard drill-down from overview to detail view
- File manager path display

---

## Button

Buttons trigger an action such as submitting a form or showing/hiding an interface component.

**Best practices:**
- Establish a clear visual hierarchy: primary (filled), secondary (outlined), tertiary (text-only)
- Use verb-first labels: 'Save changes', 'Create project', not 'Okay' or 'Submit'
- Minimum touch target of 44×44 px; desktop buttons at least 36 px tall
- Show a loading spinner inside the button during async actions — disable to prevent double-clicks
- Limit to one primary button per visible viewport section
- Ensure focus ring is visible and high-contrast for keyboard users

**Common layouts:**
- Form footer with primary action right-aligned and secondary action left-aligned
- Hero CTA button centered or left-aligned beneath headline
- Dialog footer with Cancel (secondary) and Confirm (primary)
- Floating action button (FAB) in bottom-right for mobile creation flows

---

## Button group

**Also known as:** Toolbar

A wrapper for multiple, related buttons.

**Best practices:**
- Group only related actions — unrelated buttons should be separated
- Visually connect buttons with shared border or tight spacing (1–2 px gap)
- Clearly indicate the active/selected state in toggle-style groups
- Keep the group to 2–5 buttons; more options warrant a dropdown or overflow menu

**Common layouts:**
- Text editor toolbar (bold, italic, underline)
- View switcher (grid view, list view)
- Segmented date range selector (Day, Week, Month)
- Split button with primary action and a dropdown for alternatives

---

## Card

**Also known as:** Tile

A container for content representing a single entity. e.g. a contact, article, or task.

**Best practices:**
- Use a single, clear visual hierarchy within each card: media → title → meta → action
- Keep cards a consistent height in grid layouts — use line clamping for variable text
- Make the entire card clickable when it represents a navigable entity
- Use subtle elevation (shadow) or a border — not both simultaneously
- Limit card content to essential info; let the detail page carry the rest

**Common layouts:**
- Product grid with image, title, price, and CTA
- Blog post feed with thumbnail, headline, excerpt, and date
- Dashboard KPI cards with metric, delta, and sparkline
- Team member directory with avatar, name, and role

---

## Carousel

**Also known as:** Content slider

A means of displaying multiple slides of content, one or more at a time. Navigation between slides can be controlled via swiping, scrolling, or buttons.

**Best practices:**
- Provide visible navigation arrows and pagination dots
- Support swipe gestures on touch devices
- Auto-advance only if the user hasn't interacted; pause on hover/focus
- Show a peek of the next slide to signal scrollability
- Keep slide count manageable (3–7) — carousels with many slides have low engagement
- Ensure accessibility: each slide should be reachable via keyboard

**Common layouts:**
- Hero image slideshow on a marketing homepage
- Product image gallery on a detail page
- Testimonial carousel with quote, author, and avatar
- Horizontal scrolling feature highlights in a mobile app

---

## Checkbox

An input for choosing from predefined options: in a group it allows the user to select multiple values from a list of options; when used alone, it gives a binary choice (checked/unchecked).

**Best practices:**
- Use checkboxes for multi-select, not single toggles (use a switch for on/off)
- Align the checkbox to the first line of its label, not the center
- Support indeterminate state for 'select all' when children are partially selected
- Minimum 44 px touch target including label area
- Group related checkboxes under a fieldset with a legend for accessibility

**Common layouts:**
- Filter panel with multi-select facets
- Terms & conditions single checkbox with long label
- To-do list with check/uncheck per item
- Table row multi-select with header 'select all'

---

## Color picker

An input for choosing a color.

**Best practices:**
- Provide a spectrum picker, hue slider, and direct hex/RGB input
- Include a set of preset swatches for quick selection
- Show a real-time preview of the selected color
- Support copy-paste of hex/RGB/HSL values
- Remember recently used colors for convenience

**Common layouts:**
- Design tool color picker with spectrum, sliders, and input fields
- Theme customizer with preset palette and custom override
- Annotation tool with color swatch row
- Brand settings with primary/secondary/accent color pickers

---

## Combobox

**Also known as:** Autocomplete  ·  Autosuggest

An input that behaves similarly to a select, with the addition of a free text input to filter options.

**Best practices:**
- Show suggestions after 1–2 characters to reduce noise
- Highlight matched text within each suggestion for scannability
- Allow keyboard navigation (arrow keys + Enter) through the dropdown
- Show a 'no results' message instead of an empty dropdown
- Debounce input to avoid excessive API calls (200–300 ms)

**Common layouts:**
- Search bar with autocomplete suggestions
- Address input with location suggestions
- Tag input that suggests existing tags
- Assignee picker in a project management tool

---

## Date input

A means of inputting a date — often separated into multiple individual fields for day/month/year.

**Best practices:**
- Clearly label the expected format (DD/MM/YYYY or MM/DD/YYYY)
- Use separate fields for day, month, and year for unambiguous entry
- Validate in real-time and show errors inline
- Support auto-advancing between fields when a segment is complete

**Common layouts:**
- Date of birth entry in a registration form
- Passport/ID expiry date input
- Invoice date field in a financial form

---

## Datepicker

**Also known as:** Calendar  ·  Datetime picker

A visual way to choose a date using a calendar view.

**Best practices:**
- Allow both manual text entry and calendar selection
- Clearly indicate the expected date format (e.g., MM/DD/YYYY)
- Highlight today's date and the currently selected date
- Disable dates outside the valid range
- Support keyboard navigation through the calendar grid
- For date ranges, show both start and end in a connected picker

**Common layouts:**
- Booking flow with check-in / check-out range picker
- Form field with calendar dropdown on focus
- Dashboard date range filter in a toolbar
- Event creation form with start date and optional end date

---

## Drawer

**Also known as:** Tray  ·  Flyout  ·  Sheet

A panel which slides out from the edge of the screen.

**Best practices:**
- Use drawers for secondary content or focused sub-tasks that don't warrant a full page
- Slide in from the right for detail panels, from the left for navigation
- Include a clear close button and support Escape to dismiss
- Dim the background with a semi-transparent overlay to establish focus
- Width should be 320–480 px on desktop; full-width on mobile

**Common layouts:**
- Mobile navigation menu sliding in from the left
- Shopping cart preview panel from the right
- Detail/edit panel in a master-detail layout
- Notification center sliding in from the right

---

## Dropdown menu

**Also known as:** Select menu

A menu in which options are hidden by default but can be shown by interacting with a button; it differs from a select in that it shows actions or navigation options and is not a form input.

**Best practices:**
- Group related items with separators and optional group headings
- Support keyboard navigation: arrow keys to move, Enter to select, Escape to close
- Keep the menu to 7±2 items; use sub-menus or search for longer lists
- Position the menu to avoid viewport overflow — flip to top if near bottom edge
- Indicate destructive actions in red and place them last, separated

**Common layouts:**
- User account menu in the top-right navigation
- Context menu on right-click or kebab icon
- Action menu on a table row (Edit, Duplicate, Delete)
- Sort/filter dropdown in a toolbar

---

## Empty state

An indication to the user that there is no data to display in the current view; it often includes an alternative action.

**Best practices:**
- Include a clear illustration or icon to soften the empty feeling
- Write a helpful headline explaining the empty state
- Provide a primary CTA that guides the user toward the next step
- Avoid blame — frame it positively ('No projects yet' not 'You have no projects')
- Show the empty state in-place within the container, not as a full-page takeover

**Common layouts:**
- Empty dashboard with 'Create your first project' CTA
- Search results page with 'No results found' and suggestions
- Empty inbox with illustration and encouraging message
- Empty table with inline prompt to add data

---

## Fieldset

A wrapper for related form fields.

**Best practices:**
- Use fieldsets to group related form fields under a descriptive legend
- Style the legend as a section heading within the form
- Ensure the fieldset is announced by screen readers for context

**Common layouts:**
- Address section grouping street, city, state, and zip fields
- Payment information section with card number, expiry, and CVV
- Personal details section in a multi-part form

---

## File

**Also known as:** Attachment  ·  Download

A representation of a file such as an uploaded attachment or a downloadable PDF.

**Best practices:**
- Show file type icon, name, and size clearly
- Include a download action and optionally a preview action
- Display upload date or last modified date
- Use a progress indicator during upload

**Common layouts:**
- Attachment list below a message or form
- File card with icon, name, size, and download button
- Document grid with thumbnails and metadata

---

## File upload

**Also known as:** File input  ·  File uploader  ·  Dropzone

An input which allows users to upload a file from their device.

**Best practices:**
- Support drag-and-drop with a clearly defined drop zone
- Show accepted file types and size limits before upload
- Display upload progress with a progress bar per file
- Allow cancellation of in-progress uploads
- Show a preview (thumbnail for images, icon + name for documents) after selection
- Validate file type and size client-side before uploading

**Common layouts:**
- Profile photo upload with circular crop preview
- Document attachment area in a form
- Multi-file drag-and-drop zone with file list below
- Inline file field with browse button and filename display

---

## Footer

Commonly appearing at the bottom of a page or section, a footer is used to display copyright and legal information or links to related content.

**Best practices:**
- Organize links into clear columns by category
- Include essential legal links: Privacy Policy, Terms of Service
- Keep the footer visually distinct but not distracting — muted background
- Include social links and a newsletter signup if appropriate
- Ensure the footer is accessible and links are keyboard-navigable

**Common layouts:**
- Multi-column footer with link groups, logo, and copyright
- Minimal SaaS footer with product links and social icons
- E-commerce footer with help, shipping, returns, and payment icons
- Single-line footer with copyright and key legal links

---

## Form

A grouping of input controls that allow a user to submit information to a server.

**Best practices:**
- Use a single-column layout for most forms — it's faster to scan
- Place labels above inputs for mobile-friendly forms
- Group related fields with visual proximity and optional fieldset headings
- Show inline validation on blur, not on every keystroke
- Disable the submit button until required fields are valid, or show clear errors on submit
- Keep forms as short as possible — ask only what's necessary

**Common layouts:**
- Sign-up form with name, email, password, and CTA
- Multi-step wizard form with progress indicator
- Settings form with grouped preference sections
- Contact form with name, email, subject, and message textarea

---

## Header

An element that appears across the top of all pages on a website or application; it usually contains the site name and main navigation.

**Best practices:**
- Keep the header height compact (56–72 px) to preserve content space
- Place the logo/brand on the left, primary navigation in the center or right
- Use a sticky header on long pages but consider auto-hide on scroll-down
- Ensure the mobile header collapses into a hamburger menu gracefully
- Maintain clear visual separation from page content (border-bottom or subtle shadow)

**Common layouts:**
- SaaS app header with logo, nav links, search, and user avatar
- Marketing site header with logo, nav links, and CTA button
- Dashboard header with breadcrumbs, page title, and action buttons
- Minimal header with centered logo and hamburger menu

---

## Heading

A title or caption used to introduce a new section.

**Best practices:**
- Use a strict heading hierarchy (h1 → h2 → h3) for accessibility and SEO
- Limit to one h1 per page — it's the page title
- Keep headings concise and descriptive — they're the outline of your content
- Use consistent sizing, weight, and spacing across heading levels

**Common layouts:**
- Page title (h1) with section headings (h2) and subsections (h3)
- Card title as an h3 within a page section
- Dashboard section headers separating widget groups

---

## Hero

**Also known as:** Jumbotron  ·  Banner

A large banner, usually appearing as one of the first items on a page; it often contains a full-width image.

**Best practices:**
- Lead with a compelling headline — clarity over cleverness
- Limit to one primary CTA and optionally one secondary CTA
- Use a high-quality image or illustration that reinforces the message
- Ensure text contrast against the background image (overlay or safe text zone)
- Keep hero height proportional — it should invite scrolling, not dominate the viewport

**Common layouts:**
- Split hero: headline + CTA on left, product screenshot on right
- Full-bleed background image with centered text overlay
- Minimal hero with large headline, subtext, and inline email capture
- Video background hero with centered headline and play button

---

## Icon

An icon is a graphic symbol designed to visually indicate the purpose of an interface element.

**Best practices:**
- Use a consistent icon style throughout the product (outlined or filled, not mixed)
- Size icons to align with adjacent text (typically 16–24 px)
- Pair icons with text labels for clarity — icon-only buttons need tooltips
- Use aria-hidden='true' for decorative icons and aria-label for functional ones

**Common layouts:**
- Navigation item with icon + label
- Action button with icon + text ('Download report')
- Status indicator icon beside a label (check, warning, error)
- Icon-only toolbar with tooltips

---

## Image

**Also known as:** Picture

An element for embedding images.

**Best practices:**
- Always provide meaningful alt text for accessibility
- Use responsive images (srcset) to serve appropriate sizes
- Lazy-load images below the fold for performance
- Reserve space for images before they load to prevent layout shift
- Use modern formats (WebP, AVIF) with fallbacks

**Common layouts:**
- Hero banner with full-width background image
- Product image gallery with thumbnails and zoom
- Blog post featured image above the title or below the headline
- Avatar or profile photo in a circular frame

---

## Label

**Also known as:** Form label

A text label for form inputs.

**Best practices:**
- Always associate labels with their form inputs (htmlFor / id pairing)
- Place labels above the input for vertical forms, beside for horizontal
- Mark required fields clearly (asterisk or 'required' text)
- Keep label text concise — use helper text for additional guidance

**Common layouts:**
- Form field with label above and helper text below
- Inline label beside a toggle or checkbox
- Floating label that moves to the top on input focus

---

## Link

**Also known as:** Anchor  ·  Hyperlink

A link is a reference to a resource. This can be external (e.g. a different web page) or internal (e.g. a specific element in the current document).

**Best practices:**
- Make link text descriptive — avoid 'click here' or 'learn more' in isolation
- Underline links in body text for discoverability; nav links may rely on context
- Use a distinct color from surrounding text (but avoid pure blue if it clashes with your palette)
- Show a visited state for content-heavy pages to aid navigation
- External links should indicate they open in a new tab (icon or aria-label)

**Common layouts:**
- Inline text link within a paragraph
- Standalone link beneath a card or section as a 'read more' action
- Footer link columns for site navigation
- Breadcrumb links in a hierarchy path

---

## List

Lists are used for grouping a collection of related items.

**Best practices:**
- Use consistent vertical rhythm — equal spacing between list items
- For interactive lists, ensure each row has a clear hover and active state
- Include dividers between items in dense lists; omit them in spacious ones
- Support keyboard navigation when the list is interactive
- Use virtualization (windowing) for lists exceeding ~100 items

**Common layouts:**
- Email inbox with sender, subject, preview, and timestamp per row
- Settings list with label, value/toggle, and optional chevron
- Activity feed with avatar, description, and relative timestamp
- File list with icon, name, size, and date columns

---

## Modal

**Also known as:** Dialog  ·  Popup  ·  Modal window

A modal is an interface element that appears over other content. It requires an interaction from the user before they can return to whatever is underneath.

**Best practices:**
- Use modals sparingly — only for actions that require immediate attention or focused input
- Always provide a clear close mechanism: X button, Cancel, and Escape key
- Trap focus within the modal while it's open for accessibility
- Return focus to the trigger element when the modal closes
- Keep modal content concise — if it needs scrolling, consider a full page instead
- Use a semi-transparent backdrop to dim the underlying content

**Common layouts:**
- Confirmation dialog with message and two action buttons
- Form modal for quick data entry (create, edit)
- Image/media preview lightbox
- Onboarding or announcement modal with illustration and CTA

---

## Navigation

**Also known as:** Nav  ·  Menu

A container for navigation links; these can be to other pages or to elements within the current page.

**Best practices:**
- Limit primary navigation to 5–7 items; group the rest under 'More' or sub-menus
- Clearly indicate the current/active page in the navigation
- Use consistent iconography alongside text labels for scannability
- Collapse to a hamburger or bottom tab bar on mobile
- Ensure all navigation items are reachable via keyboard (Tab + Enter)

**Common layouts:**
- Horizontal top nav with logo, links, and user menu
- Vertical sidebar navigation with icon + label and collapsible groups
- Bottom tab bar for mobile apps (Home, Search, Create, Notifications, Profile)
- Mega-menu dropdown with categorized link columns

---

## Pagination

Pagination is the process of splitting information over multiple pages instead of showing it all on a single page; also the name for the interface component used for navigating between these pages.

**Best practices:**
- Show first, last, and a window of pages around the current one
- Use ellipsis to indicate skipped pages, not dozens of page numbers
- Provide Previous/Next buttons in addition to numbered pages
- Clearly style the current page as selected
- Consider infinite scroll or 'Load more' for content feeds

**Common layouts:**
- Table footer with page numbers, rows-per-page selector, and total count
- Search results pagination centered below the results list
- Blog archive with Previous/Next navigation
- API documentation with page controls at top and bottom

---

## Popover

An element that pops up from another element over other content; it differs from a tooltip in that it is usually triggered via click instead of hover and can contain interactive elements.

**Best practices:**
- Trigger via click, not hover, to support touch devices and accessibility
- Position intelligently to avoid clipping at viewport edges
- Include a subtle arrow/caret pointing to the trigger element
- Dismiss when clicking outside or pressing Escape
- Keep popover content brief — it's not a modal

**Common layouts:**
- Color picker dropdown triggered by a swatch
- User profile preview card on avatar hover/click
- Quick-edit popover for inline data modification
- Help tooltip with rich content (text + link)

---

## Progress bar

**Also known as:** Progress

A horizontal bar indicating the current completion status of a long-running task, usually updated continuously as the task progresses.

**Best practices:**
- Show a determinate bar when progress is measurable, indeterminate when unknown
- Include a percentage label for accessibility and clarity
- Use color to indicate state: blue/green for normal, red for error, amber for warning
- Animate smoothly — avoid jarring jumps between values
- Keep the bar visually proportional to its container (not too thin to see)

**Common layouts:**
- File upload progress beneath the file name
- Onboarding completion bar in a sidebar or header
- Course progress bar at the top of a lesson page
- System resource usage bar in a monitoring dashboard

---

## Progress indicator

**Also known as:** Progress tracker  ·  Stepper  ·  Steps  ·  Timeline  ·  Meter

A representation of a user's progress through a series of discrete steps.

**Best practices:**
- Clearly distinguish completed, current, and upcoming steps
- Use numbered or labeled steps — not just dots
- Allow users to click back to completed steps if the flow permits
- Keep the total step count visible so users know the scope
- Vertically stack steps on mobile for readability

**Common layouts:**
- Multi-step checkout (Cart → Shipping → Payment → Confirmation)
- Account setup wizard with profile, preferences, and verification
- Application form with multiple sections
- Project timeline with milestones

---

## Quote

**Also known as:** Pull quote  ·  Block quote

Quotes are used to display a quotation: either from a person or another outside source or to highlight a passage of the current document.

**Best practices:**
- Use a distinct visual treatment — large quotation marks, left border, or italic text
- Always attribute the quote to its source
- Keep pull quotes short — they're attention-grabbers, not paragraphs

**Common layouts:**
- Testimonial block with photo, quote, name, and title
- Pull quote in a blog post breaking up long text
- Customer quote in a case study with company logo

---

## Radio button

**Also known as:** Radio  ·  Radio group

Radio buttons allow a user to select a single option from a list of predefined options.

**Best practices:**
- Use radio buttons for mutually exclusive choices (select one from many)
- Always pre-select a sensible default when possible
- Group under a fieldset with a legend describing the choice
- Stack vertically for more than 2 options — horizontal only for 2–3 short-label options
- Provide sufficient spacing between options (at least 8 px) for easy tapping

**Common layouts:**
- Shipping method selection (Standard, Express, Overnight)
- Payment method chooser with radio + icon + description
- Survey question with single-choice answers
- Plan/tier selection in a pricing form

---

## Rating

Ratings let users see and/or set a star rating for a product or other item.

**Best practices:**
- Use 5-star scale as the widely understood standard
- Allow half-star precision for display; use full stars for input
- Show the average rating and total review count together
- Use filled/empty stars with sufficient color contrast

**Common layouts:**
- Product rating display with stars and review count
- Review submission with interactive star input and text area
- Summary rating card with distribution bar chart

---

## Rich text editor

**Also known as:** RTE  ·  WYSIWYG editor

An interface for editing rich text content (with formatting), usually through a WYSIWYG interface.

**Best practices:**
- Provide a minimal default toolbar — reveal advanced formatting on demand
- Support keyboard shortcuts for common formatting (Cmd+B, Cmd+I)
- Ensure pasted content is sanitized to prevent layout-breaking HTML
- Show a word/character count for content with limits

**Common layouts:**
- Blog post editor with formatting toolbar and preview
- Email composer with rich text and attachment support
- Comment editor with basic formatting (bold, italic, link, list)

---

## Search input

**Also known as:** Search

Search inputs allow users to find content by entering a search term.

**Best practices:**
- Place a magnifying glass icon inside the field to signal purpose
- Support Cmd/Ctrl+K as a global shortcut to focus the search
- Show recent searches and suggested queries in a dropdown
- Debounce input and show a loading indicator during server queries
- Provide a clear/reset button (×) once text is entered

**Common layouts:**
- Global search in the top navigation bar
- Command palette overlay (Cmd+K) with categorized results
- Inline search/filter above a data table
- Full-page search with prominent input and categorized results below

---

## Segmented control

**Also known as:** Toggle button group

A hybrid somewhere between a button group, radio buttons, and tabs; segmented controls are used to switch between different options or views.

**Best practices:**
- Limit to 2–5 segments — more options warrant tabs or a dropdown
- Use equal-width segments for visual balance
- Animate the selection indicator sliding between options
- Ensure the selected state has strong contrast against unselected
- Use sentence case for segment labels

**Common layouts:**
- Map/list/grid view switcher
- Billing period toggle (Monthly / Annually)
- Light/dark mode toggle in settings
- Chart type selector (Line, Bar, Pie)

---

## Select

**Also known as:** Dropdown  ·  Select input

A form input used for selecting a value: when collapsed it shows the currently selected option and when expanded, it shows a scrollable list of predefined options.

**Best practices:**
- Use native select for simple use cases (better accessibility and mobile UX)
- For custom selects, ensure full keyboard support and ARIA attributes
- Show a placeholder label ('Select an option…') when no value is chosen
- Group long option lists with optgroups or headings
- For searchable selects with many options, combine with combobox behavior

**Common layouts:**
- Country/region picker in an address form
- Sort-by dropdown in a product listing toolbar
- Role selector in a user invitation flow
- Language/locale switcher

---

## Separator

**Also known as:** Divider  ·  Horizontal rule  ·  Vertical rule

A separator between two elements, usually consisting of a horizontal line.

**Best practices:**
- Use subtle, low-contrast separators — they guide the eye, not dominate it
- Prefer spacing over separators when grouping is already clear
- Use horizontal rules between content sections, vertical rules between columns

**Common layouts:**
- Horizontal divider between list items or content sections
- Vertical separator between sidebar and main content
- Section divider with centered label ('or', 'related content')

---

## Skeleton

**Also known as:** Skeleton loader

A placeholder layout for content which hasn't yet loaded, usually built up of grey boxes.

**Best practices:**
- Match the skeleton shape to the actual content layout as closely as possible
- Use a subtle shimmer/pulse animation to indicate loading — not a spinner
- Avoid skeletons for very fast loads (<300 ms) — they add visual noise
- Show skeleton immediately on navigation; replace atomically when data arrives
- Use muted, low-contrast colors (light gray on white) for skeleton blocks

**Common layouts:**
- Card grid skeleton with image placeholder, title bar, and text lines
- List/feed skeleton with repeating row shapes
- Profile page skeleton with avatar circle and text blocks
- Dashboard skeleton with chart placeholder and metric blocks

---

## Skip link

Links within a page for skipping to another section, primarily for users who navigate using a keyboard.

**Best practices:**
- Make it the first focusable element in the DOM
- Visually hidden until focused — then clearly visible
- Link to the main content area with a descriptive label ('Skip to main content')

**Common layouts:**
- Hidden link that appears on Tab focus at the very top of the page

---

## Slider

**Also known as:** Range input

A form control for choosing a value within a preset range of values.

**Best practices:**
- Show the current value in a tooltip or adjacent label
- Use tick marks for discrete value sliders
- Support both dragging and clicking on the track to set value
- Ensure minimum touch target size for the thumb (44 px)
- Pair with a text input for precise value entry when needed

**Common layouts:**
- Price range filter with dual thumbs (min/max)
- Volume/brightness control slider
- Image crop zoom level control
- Pricing page seat/usage slider with dynamic price display

---

## Spinner

**Also known as:** Loader  ·  Loading

A visual indicator that a process is happening in the background but the interface is not yet ready for interaction.

**Best practices:**
- Show spinners only after a delay (~300 ms) to avoid flicker on fast responses
- Size the spinner proportionally to the context: inline (16 px), button (20 px), page (40+ px)
- Use a single brand-consistent spinner design throughout the app
- Provide an aria-label or sr-only text for screen readers ('Loading…')
- Prefer skeleton screens over spinners when the layout is predictable

**Common layouts:**
- Centered full-page spinner during initial app load
- Inline spinner inside a button during form submission
- Small spinner beside a table cell during lazy-loaded data fetch
- Overlay spinner on a card while its content refreshes

---

## Stack

A wrapper component for adding a consistent margin between components.

**Best practices:**
- Use a consistent spacing scale (4, 8, 12, 16, 24, 32, 48 px)
- Default to vertical stacking; support horizontal for inline element groups
- Use stack as a layout primitive to enforce consistent spacing across components

**Common layouts:**
- Vertical stack of form fields with uniform gap
- Horizontal stack of action buttons with gap
- Card content layout with vertical stack of title, description, and meta

---

## Stepper

**Also known as:** Nudger  ·  Quantity  ·  Counter

A control for editing a numeric value with buttons for decrementing / incrementing.

**Best practices:**
- Use clear +/- buttons with adequate touch targets
- Allow direct number entry in addition to button interaction
- Set sensible min, max, and step values
- Disable the relevant button when at min or max value

**Common layouts:**
- Quantity selector in an e-commerce cart
- Number input for seat count in a booking flow
- Portion size adjuster in a recipe app

---

## Table

A component for displaying large amounts of data in rows and columns; commonly referred to as a 'Data Table' when it includes sorting and/or filtering functionality.

**Best practices:**
- Use a sticky header row for scrollable tables
- Right-align numeric columns for easy comparison
- Provide sortable column headers with clear sort direction indicators
- Alternate row colors (zebra striping) or use horizontal dividers for readability
- Include a bulk-select checkbox column for actionable tables
- Make tables horizontally scrollable on mobile rather than hiding columns

**Common layouts:**
- Admin data table with search, filters, sort, pagination, and row actions
- Pricing comparison table with feature rows and plan columns
- Financial ledger with date, description, amount, and running balance
- Leaderboard table with rank, name, avatar, and score

---

## Tabs

**Also known as:** Tabbed interface

Tabbed interfaces are a way of navigating between multiple panels, reducing clutter and fitting more into a smaller space.

**Best practices:**
- Limit to 2–7 tabs; more options need a scrollable tab bar or dropdown overflow
- Clearly indicate the active tab with a bottom border, background fill, or bold text
- Use short, descriptive tab labels (1–2 words)
- Place tab content immediately below the tab bar with no visual gap
- Support keyboard navigation: arrow keys between tabs, Tab to content
- Consider swapping tabs for an accordion on narrow viewports

**Common layouts:**
- Product page with Description, Reviews, and Specifications tabs
- Settings page with General, Security, Notifications sections
- Profile page with Activity, Projects, and Settings tabs
- Dashboard with different report views (Overview, Analytics, Logs)

---

## Text input

A form control that accepts a single line of text.

**Best practices:**
- Use appropriate input types (email, tel, url, number) for mobile keyboard optimization
- Show placeholder text only as an example format, never as a label replacement
- Display character count for length-limited fields
- Show inline validation errors below the input with a red border and message
- Support autofill attributes for common fields (name, email, address)

**Common layouts:**
- Login form with email and password inputs
- Search bar with icon prefix and clear button
- Inline edit field that converts from text to input on click
- Settings form with labeled text inputs in a single column

---

## Textarea

**Also known as:** Textbox  ·  Text box

A form control for editing multi-line text.

**Best practices:**
- Allow vertical resizing but consider setting a min and max height
- Show character count if there's a limit
- Use a taller default height (3–5 rows) to signal multi-line input is expected
- Auto-grow the textarea as the user types for a smoother experience

**Common layouts:**
- Comment or reply input below a post
- Feedback form with a large message area
- Note-taking field in a CRM or project tool
- Code or JSON input with monospace font

---

## Toast

**Also known as:** Snackbar

A type of alert which appears in a layer above other content, visually similar to a mobile or desktop push notification.

**Best practices:**
- Auto-dismiss after 4–6 seconds for non-critical toasts
- Allow manual dismissal with a close button or swipe
- Stack multiple toasts with the newest on top
- Position in a consistent corner — bottom-right is most common for desktop
- Include an action link for undoable operations ('Undo' for delete)
- Limit to one line of text — toasts are for brief confirmations

**Common layouts:**
- Success toast after saving a form ('Changes saved')
- Error toast with retry action after a failed request
- Undo toast after deleting an item ('Item deleted. Undo')
- Notification toast with avatar and brief message preview

---

## Toggle

**Also known as:** Switch  ·  Lightswitch  ·  Toggle button

A control used to switch between two states: often on or off.

**Best practices:**
- Use for binary on/off settings that take effect immediately
- Label the toggle with what it controls, not 'On/Off'
- Show the current state visually (color, position) and with an optional text label
- Size the toggle to be easily tappable (44+ px wide)
- Avoid using toggles inside forms that require a Save action — use checkboxes instead

**Common layouts:**
- Settings row with label on the left and toggle on the right
- Dark mode toggle in a header or settings panel
- Feature flag toggles in an admin panel
- Notification preference toggles in a list

---

## Tooltip

**Also known as:** Toggletip

A means of displaying a description or extra information about an element, usually on hover, but can also be on click or tap.

**Best practices:**
- Use tooltips for supplementary info — never for essential content
- Trigger on hover (desktop) and long-press (mobile); avoid click-to-show
- Show after a short delay (~300 ms) and hide on mouse leave
- Keep tooltip text to a single sentence or a few words
- Position to avoid obscuring the trigger element or important content
- Use a toggletip (click-triggered) when the content includes interactive elements

**Common layouts:**
- Icon button tooltip showing the action name
- Truncated text tooltip revealing the full string on hover
- Info icon tooltip explaining a form field's purpose
- Chart data point tooltip showing exact values

---

## Tree view

A component for displaying nested hierarchical information, such as a table of contents or directory structure.

**Best practices:**
- Use indentation (16–24 px per level) to show hierarchy
- Include expand/collapse toggles (chevron or triangle) for parent nodes
- Support keyboard navigation: arrows to traverse, Enter to select, +/- to expand/collapse
- Highlight the selected node and show a focus indicator
- Lazy-load deep children for performance in large trees

**Common layouts:**
- File/folder browser in a code editor or CMS
- Category tree in an e-commerce sidebar
- Organization chart or reporting hierarchy
- Table of contents navigation for documentation

---

## Video

**Also known as:** Video player

Video players are used for displaying video content; they often include controls to control playback.

**Best practices:**
- Show a poster/thumbnail image before playback
- Include captions/subtitles for accessibility
- Provide standard controls: play/pause, volume, fullscreen, progress bar
- Lazy-load video content and avoid autoplay with sound

**Common layouts:**
- Product demo video centered on a landing page
- Video player with title, description, and related videos
- Background video hero with muted autoplay
- Tutorial video embedded in documentation

---

## Visually hidden

**Also known as:** Screenreader only

Invisible text used to provide extra context for users of assistive technology.

**Best practices:**
- Use for screen-reader-only text that provides context invisible users don't need
- Never use display:none or visibility:hidden — use a clip-rect technique
- Apply to skip links, icon-only button labels, and form field instructions

**Common layouts:**
- Hidden label for an icon-only close button
- Screen-reader instructions for a complex widget

---
