# Campus AI Assistant - Axure RP 10 Prototype

## File: CampusAIAssistant.rp

This directory should contain the Axure RP 10 prototype file (`CampusAIAssistant.rp`).

### Building the Prototype

Follow the steps in `docs/axure-build-steps.md` to create the prototype using Axure RP 10:

1. **Create Masters** (reusable components):
   - DesktopFrame (main layout with header, sidebar, content area)
   - ChatBubble (for AI chat messages)
   - ListItem (for repeater items)
   - SearchBar (for search functionality)

2. **Setup Global Variables**:
   - gUserId (user ID)
   - gUserRole (student/teacher)
   - gUserName (user display name)
   - gLastIntent (last detected intent for context)
   - gLoading (loading state flag)
   - gTheme ("light" or "dark")

3. **Create Pages**:
   - 01_Login
   - 02_Home_Dashboard
   - 03_Assistant_Chat
   - 04_Courses
   - 05_Notices
   - 06_Reservations
   - 07_Canteen
   - 08_Map
   - 09_Tickets
   - 10_Profile

4. **Import Data**:
   - Import CSV files from `data/` directory into respective Repeater widgets
   - faqs.csv → rpHints/FAQ matching
   - courses.csv → rpCourses
   - notices.csv → rpNotices
   - rooms.csv → rpRooms
   - canteen.csv → rpDishes
   - map_pois.csv → rpPOI
   - conversations_seed.csv → rpChat initial messages

5. **Implement Dark Mode**:
   - Add theme toggle button in header
   - Create ApplyTheme interaction that updates colors based on gTheme
   - Use color tokens from `docs/styles.md`

6. **Setup AI Chat Interactions**:
   - Implement intent detection based on keywords/FAQ matching
   - Add thinking animation (dpThinking panel)
   - Create dynamic responses with action buttons
   - Add suggestion hints that filter as user types

### Design Specifications

- **Canvas**: 1440px width for desktop
- **Layout**: Header (64px) + Sidebar (240px) + Main content area
- **Style**: Apple Human Interface Guidelines (clarity, deference, depth)
- **Fonts**: SF font stack (see `docs/styles.md`)
- **Colors**: Light/Dark mode tokens (see `docs/styles.md`)
- **Logo**: Use `assets/logo.png` in top-left of header

### Testing

After creating the prototype, test according to scenarios in `docs/qa/test-scenarios.md`:
1. Course queries (natural language)
2. Room reservations (parameter extraction)
3. Notice summaries
4. Canteen recommendations (dietary preferences)
5. Map routes
6. Ticket submission
7. Suggestion hints
8. Role switching (teacher mode)
9. Fallback responses

### File Format

The `.rp` file must be:
- Created with Axure RP 10 (not earlier versions)
- Configured for PC web only (not mobile)
- Stored with Git LFS (configured in `.gitattributes`)
