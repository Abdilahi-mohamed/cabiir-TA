# Cabiir Travel Agency - Comprehensive Codebase Analysis

---

## 1. COMPLETE LIST OF ALL CSS FILES AND THEIR CONTENT

### File Structure
```
frontend/src/
├── App.css (Main application styles)
├── index.css (Global styles)
├── auth.css (Authentication page styles)
├── features.css (Component-specific styles)
└── landing.css (Landing page styles)
```

---

### A. App.css (Main Application Stylesheet)
**Location:** [frontend/src/App.css](frontend/src/App.css)

**Purpose:** Contains all core application styling including sidebar, dashboard layout, tables, forms, and responsive design.

**Key Sections:**
- Root variables and base layout
- Sidebar styling (with branch-specific gradients for Hargeisa and Jidda)
- Brand/logo styling
- Manager profile section
- Navigation buttons
- Table and form styling
- Responsive design breakpoints

**Full Content:**
```css
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&display=swap');
:root { --ink:#16313a; --muted:#789096; --line:#e4eded; --teal:#087c80; --paper:#fff; } 
.app { min-height:100vh; display:flex; background:#f6f9f9; } 
.sidebar { width:265px; flex:none; color:#dcebed; padding:26px 16px 18px; display:flex; flex-direction:column; background:linear-gradient(160deg,#0d475b,#087d80 65%,#0b6b75); } 
.jidda .sidebar { background:linear-gradient(160deg,#243c62,#346696 70%,#527db0); } 
.brand,.manager,.header-actions,.form-heading,.table-heading { display:flex; align-items:center; } 
.brand { gap:10px; padding:0 10px 31px; } 
.brand-mark { display:grid; place-items:center; width:37px; height:37px; border:2px solid #b7e2df; border-radius:11px; font-size:24px; font-weight:700; color:#fff; } 
.brand strong { display:block; color:#fff; font-size:20px; }
.brand small,.manager small { display:block; font-size:10px; opacity:.65; }
.close-nav { display:none; margin-left:auto; background:none; color:white; border:0; font-size:24px; } 
.manager { gap:10px; padding:13px 10px; border:1px solid #ffffff27; border-radius:12px; margin-bottom:29px; }
.manager img { width:38px; height:38px; border-radius:50%; object-fit:cover; border:2px solid #b5dedc; }
.manager strong { display:block; font-size:12px; margin-top:2px; color:#fff; }
.upload { margin-left:auto; font-size:11px; color:#c4ece9; cursor:pointer; }
.upload input { display:none; } 
.nav-label { padding:0 11px 9px; text-transform:uppercase; letter-spacing:1.2px; font-size:10px; color:#94c8ca; }
.form-label { margin-top:26px; } 
nav { display:grid; gap:4px; }
.sidebar button { text-align:left; border:0; background:transparent; color:#c9e1e1; border-radius:8px; padding:11px 12px; cursor:pointer; font-size:13px; }
.sidebar nav button { display:flex; gap:13px; align-items:center; }
.sidebar nav button span,.side-create span { width:16px; color:#8ed0ce; }
.sidebar nav button.active { color:white; background:#ffffff1c; font-weight:600; box-shadow:inset 3px 0 #f6ae66; }
.side-create { width:100%; padding:8px 12px!important; font-size:12px; }
.sidebar { overflow-y:auto; }
.nav-overview { width:100%; margin-bottom:20px; text-align:left; border:0; background:transparent; color:#c9e1e1; border-radius:8px; padding:12px; cursor:pointer; font-size:14px; font-weight:700; }
.nav-overview.active { color:#fff; background:#ffffff1c; box-shadow:inset 3px 0 #f6ae66; }
.workspace-label { margin-top:24px; }
.other-label { margin-top:22px; }
.overview-grid { grid-template-columns:repeat(3,1fr); }
.paid-checkbox { width:20px; height:20px; accent-color:#087c80; cursor:pointer; transform:scale(1.15); }
.users-action { white-space:nowrap; }
.sidebar { position:sticky; top:0; height:100vh; overflow-y:auto; }
.nav-overview { order:1; }
.form-label { order:2; }
.sidebar > .side-create { order:3; }
.workspace-label { order:4; }
.sidebar > nav { order:5; }
.other-label { order:6; }
.other-label + .side-create { order:7; }
.sidebar > button.side-create:nth-of-type(2) { order:3; }
.sidebar > button.side-create:nth-of-type(3) { order:3; }
.sidebar > button.side-create:nth-of-type(4) { order:3; }
.sidebar > button.side-create:nth-of-type(5) { order:7; }
.sidebar > button.side-create:nth-of-type(6) { order:8; }
.jidda .sidebar > button.side-create { order:8; }
.sidebar-footer { order:9; margin-top:auto; }
.nav-label { font-size:11px; font-weight:700; color:#b0dcdb; }
.overview-grid { grid-template-columns:repeat(3,1fr); }
.paid-checkbox { width:20px; height:20px; accent-color:#087c80; cursor:pointer; transform:scale(1.15); }
.users-action { white-space:nowrap; }
.brand-upload { cursor:pointer; }
.brand-upload input { display:none; }
.brand-upload .brand-mark { overflow:hidden; }
.brand-upload .brand-mark img { width:100%; height:100%; object-fit:cover; }
.has-dashboard-logo .app .brand-mark { color:transparent; background:var(--dashboard-logo) center/cover no-repeat; border-color:#b7e2df; }
.manager strong { cursor:pointer; }
.manager strong:hover { color:#d2f2ef; }
@media (max-width:900px) { .overview-grid { grid-template-columns:repeat(2,1fr); } }
.form-grid input[type=number] { appearance:textfield; }
.form-grid input[type=number]::-webkit-inner-spin-button { opacity:1; }
@media (max-width:650px) { .overview-grid { grid-template-columns:1fr; }.nav-overview { margin-bottom:12px; } }
```

---

### B. index.css (Global Styles)
**Location:** [frontend/src/index.css](frontend/src/index.css)

**Purpose:** Global typography, base element styling, and fundamental layout rules.

**Full Content:**
```css
:root { 
  font-family: 'DM Sans', 'Segoe UI', sans-serif; 
  color: #152b35; 
  background: #f5f8f8; 
  font-synthesis: none; 
  text-rendering: optimizeLegibility; 
  -webkit-font-smoothing: antialiased; 
} 
* { 
  box-sizing: border-box; 
} 
body { 
  margin: 0; 
  min-width: 320px; 
  min-height: 100vh; 
} 
button, input { 
  font: inherit; 
}
```

---

### C. auth.css (Authentication Styling)
**Location:** [frontend/src/auth.css](frontend/src/auth.css)

**Purpose:** Styles for login and authentication pages.

**Full Content:**
```css
.auth-page { 
  min-height:100vh; 
  display:grid; 
  place-items:center; 
  padding:24px; 
  background:radial-gradient(circle at 15% 15%,#dff4f5,transparent 35%),linear-gradient(135deg,#f8fcfc,#e5f2f7); 
  position:relative; 
}
.auth-back { 
  position:absolute; 
  top:28px; 
  left:5%; 
  border:0; 
  background:none; 
  color:#4f7079; 
  cursor:pointer; 
}
.auth-card { 
  width:min(100%,430px); 
  padding:36px; 
  background:#fff; 
  border:1px solid #dcebed; 
  border-radius:16px; 
  box-shadow:0 22px 60px #1c65701a; 
}
.auth-logo { 
  display:flex; 
  align-items:center; 
  gap:10px; 
  margin-bottom:28px; 
  color:#16313a; 
  font-size:21px; 
}
.auth-card h1 { 
  margin:12px 0 8px; 
  font-size:30px; 
}
.auth-card > p { 
  color:#789096; 
  font-size:13px; 
  line-height:1.6; 
  margin-bottom:23px; 
}
.auth-card form { 
  display:grid; 
  gap:15px; 
}
.auth-card label { 
  display:grid; 
  gap:7px; 
}
.auth-card label span { 
  color:#48646b; 
  font-size:12px; 
  font-weight:600; 
}
.auth-card input,.auth-card select { 
  width:100%; 
  border:1px solid #d7e3e3; 
  border-radius:7px; 
  padding:12px; 
  color:#16313a; 
  outline-color:#087c80; 
}
.auth-submit { 
  width:100%; 
  margin-top:7px; 
}
.auth-error { 
  margin:12px 0; 
  padding:11px; 
  border-radius:7px; 
  background:#fff1ef; 
  color:#b4524b; 
  font-size:12px; 
}
.auth-switch { 
  border:0; 
  background:transparent; 
  color:#087c80; 
  width:100%; 
  margin-top:19px; 
  cursor:pointer; 
  font-size:12px; 
  font-weight:700; 
}
```

---

### D. features.css (Component Features & Layout)
**Location:** [frontend/src/features.css](frontend/src/features.css)

**Purpose:** Specific styling for dashboard components, tables, forms, and responsive behavior.

**Full Content:**
```css
.sidebar { overflow-y:auto; }
.nav-overview { width:100%; margin-bottom:20px; text-align:left; border:0; background:transparent; color:#c9e1e1; border-radius:8px; padding:12px; cursor:pointer; font-size:14px; font-weight:700; }
.nav-overview.active { color:#fff; background:#ffffff1c; box-shadow:inset 3px 0 #f6ae66; }
.workspace-label { margin-top:24px; }
.other-label { margin-top:22px; }
.overview-grid { grid-template-columns:repeat(3,1fr); }
.paid-checkbox { width:20px; height:20px; accent-color:#087c80; cursor:pointer; transform:scale(1.15); }
.users-action { white-space:nowrap; }
 .sidebar { position:sticky; top:0; height:100vh; overflow-y:auto; }
.nav-overview { width:100%; margin-bottom:20px; text-align:left; border:0; background:transparent; color:#c9e1e1; border-radius:8px; padding:12px; cursor:pointer; font-size:14px; font-weight:700; order:1; }
.nav-overview.active { color:#fff; background:#ffffff1c; box-shadow:inset 3px 0 #f6ae66; }
.form-label { order:2; }
.sidebar > .side-create { order:3; }
.workspace-label { margin-top:24px; order:4; }
.sidebar > nav { order:5; }
.other-label { margin-top:22px; order:6; }
.other-label + .side-create { order:7; }
.sidebar > button.side-create:nth-of-type(2) { order:3; }
.sidebar > button.side-create:nth-of-type(3) { order:3; }
.sidebar > button.side-create:nth-of-type(4) { order:3; }
.sidebar > button.side-create:nth-of-type(5) { order:7; }
.sidebar > button.side-create:nth-of-type(6) { order:8; }
.jidda .sidebar > button.side-create { order:8; }
.sidebar-footer { order:9; margin-top:auto; }
.nav-label { font-size:11px; font-weight:700; color:#b0dcdb; }
.overview-grid { grid-template-columns:repeat(3,1fr); }
.paid-checkbox { width:20px; height:20px; accent-color:#087c80; cursor:pointer; transform:scale(1.15); }
.users-action { white-space:nowrap; }
.brand-upload { cursor:pointer; }
.brand-upload input { display:none; }
.brand-upload .brand-mark { overflow:hidden; }
.brand-upload .brand-mark img { width:100%; height:100%; object-fit:cover; }
.has-dashboard-logo .app .brand-mark { color:transparent; background:var(--dashboard-logo) center/cover no-repeat; border-color:#b7e2df; }
.manager strong { cursor:pointer; }
.manager strong:hover { color:#d2f2ef; }
@media (max-width:900px) { .overview-grid { grid-template-columns:repeat(2,1fr); } }
.form-grid input[type=number] { appearance:textfield; }
.form-grid input[type=number]::-webkit-inner-spin-button { opacity:1; }
@media (max-width:650px) { .overview-grid { grid-template-columns:1fr; }.nav-overview { margin-bottom:12px; } }
```

---

### E. landing.css (Landing Page Styling)
**Location:** [frontend/src/landing.css](frontend/src/landing.css)

**Purpose:** Styling for the public-facing landing page before authentication.

**Full Content:**
```css
.landing { 
  min-height:100vh; 
  color:#122f3b; 
  background:radial-gradient(circle at 80% 18%,#e4f5fb 0,transparent 32%),linear-gradient(135deg,#fff 0%,#f5fbfc 52%,#e5f3f8 100%); 
}
.landing-header { 
  height:82px; 
  padding:0 5%; 
  display:flex; 
  align-items:center; 
  justify-content:space-between; 
  background:#ffffffd9; 
  border-bottom:1px solid #dcebed; 
}
.landing-brand { 
  display:flex; 
  align-items:center; 
  gap:10px; 
  font-size:21px; 
}
.landing-brand strong { 
  letter-spacing:-.5px; 
}
.landing-header nav { 
  display:flex; 
  align-items:center; 
  gap:32px; 
}
.landing-header nav a { 
  color:#47646d; 
  text-decoration:none; 
  font-size:13px; 
}
.landing-header nav button { 
  border:0; 
  background:transparent; 
  color:#087c80; 
  cursor:pointer; 
  font-size:13px; 
  font-weight:700; 
}
.landing-hero { 
  max-width:1260px; 
  min-height:calc(100vh - 135px); 
  margin:auto; 
  padding:70px 5% 35px; 
  display:grid; 
  grid-template-columns:1fr 1fr; 
  align-items:center; 
  gap:5%; 
}
.hero-copy { 
  max-width:570px; 
}
.hero-copy h1 { 
  margin:18px 0; 
  font-size:clamp(34px,5vw,66px); 
  line-height:1.05; 
  letter-spacing:-2px; 
}
.hero-copy h1 b { 
  color:#087c80; 
  font-weight:700; 
}
.hero-copy p { 
  max-width:560px; 
  color:#5b7379; 
  font-size:16px; 
  line-height:1.8; 
}
.landing-button { 
  margin-top:30px; 
  padding:15px 22px; 
}
.logo-panel { 
  min-height:390px; 
  position:relative; 
  display:grid; 
  place-items:center; 
  border-radius:28px; 
  background:linear-gradient(145deg,#dff4f5,#c6e9f3 60%,#dce9fa); 
  box-shadow:inset 0 0 0 1px #fff,0 24px 60px #1770801a; 
}
.cabiir-logo { 
  width:min(72%,360px); 
  aspect-ratio:320/190; 
  background:url('/cabiir-logo.svg') center/contain no-repeat; 
  filter:drop-shadow(0 16px 15px #173f4c24); 
}
.cabiir-logo > * { 
  display:none; 
}
.route { 
  position:absolute; 
  padding:10px 13px; 
  background:#ffffffbd; 
  border:1px solid #fff; 
  border-radius:30px; 
  color:#087c80; 
  font-size:11px; 
  box-shadow:0 8px 22px #155e7020; 
}
.route-one { 
  top:20%; 
  right:8%; 
}
.route-two { 
  bottom:18%; 
  left:8%; 
}
.landing-footer { 
  max-width:1260px; 
  margin:auto; 
  padding:0 5% 22px; 
  display:flex; 
  justify-content:space-between; 
  color:#779198; 
  font-size:11px; 
}
@media (max-width:650px) { 
  .landing-header { height:70px; }
  .landing-header nav a { display:none; }
  .landing-header nav { gap:0; }
  .landing-hero { min-height:calc(100vh - 100px); padding:45px 6% 25px; grid-template-columns:1fr; gap:35px; }
  .hero-copy h1 { font-size:39px; letter-spacing:-1px; }
  .hero-copy p { font-size:14px; line-height:1.65; }
  .logo-panel { min-height:275px; }
  .cabiir-logo { width:70%; }
  .landing-footer { display:none; } 
}
```

---

## 2. REGISTRATION TABLE COMPONENT - LOCATION AND DETAILS

### Component Location
**File:** [frontend/src/App.tsx](frontend/src/App.tsx)  
**Function Name:** `RegistrationTable`  
**Approximate Line:** Line 54

### Component Code:
```jsx
function RegistrationTable({ 
  type, 
  records, 
  openForm, 
  remove, 
  updatePaid 
}: { 
  type: RegistrationType; 
  records: Registration[]; 
  openForm: (type: RegistrationType, record?: Registration) => void; 
  remove: (type: RegistrationType, id: string) => void; 
  updatePaid: (type: RegistrationType, id: string, paid: boolean) => void 
}) { 
  return (
    <section className="content">
      <div className="table-heading">
        <div>
          <span className="eyebrow">Shared records</span>
          <h2>{labels[type]} registrations</h2>
          <p>Records are visible to both branches.</p>
        </div>
        <button className="primary" onClick={() => openForm(type)}>
          ＋ Add {labels[type]}
        </button>
      </div>
      <div className="table-wrap">
        <table>
          <thead>
            <tr>
              <th>Customer</th>
              <th>Phone</th>
              <th>Reference</th>
              <th>Money amount</th>
              <th>Paid</th>
              <th>Actions</th>
            </tr>
          </thead>
          <tbody>
            {records.length ? 
              records.map(record => (
                <tr key={record._id}>
                  <td>
                    <strong>{record.fullName}</strong>
                    <small>{record.passportNumber}</small>
                  </td>
                  <td>{record.phone}</td>
                  <td>{record.reference || '—'}</td>
                  <td>${(record.moneyAmount || 0).toLocaleString()}</td>
                  <td>
                    <input 
                      className="paid-checkbox" 
                      type="checkbox" 
                      checked={Boolean(record.paid)} 
                      onChange={event => updatePaid(type, record._id, event.target.checked)} 
                      aria-label={`Paid for ${record.fullName}`} 
                    />
                  </td>
                  <td>
                    <button className="action" onClick={() => openForm(type, record)}>Edit</button>
                    <button className="action danger" onClick={() => remove(type, record._id)}>Delete</button>
                  </td>
                </tr>
              )) 
              : <tr><td colSpan={6} className="empty">No registrations yet.</td></tr>
            }
          </tbody>
        </table>
      </div>
    </section>
  )
}
```

### Passport Number Column - Details

**Location in table:** First column (`<th>Customer</th>`)

**HTML Structure:**
```jsx
<td>
  <strong>{record.fullName}</strong>
  <small>{record.passportNumber}</small>
</td>
```

**Handling Details:**
- The passport number is stored in the `record.passportNumber` property
- It's displayed as a `<small>` tag underneath the full name in the first table column
- The passport number is part of the `Registration` type which includes:
  - `_id`: string
  - `fullName`: string
  - `phone`: string
  - `passportNumber`: string
  - `date`: string
  - `goDate`: string
  - `backDate`: string
  - `hotel?`: string
  - `places?`: string
  - `reference`: string
  - `moneyAmount`: number
  - `paid`: boolean
  - `createdAt?`: string

**Type Definition (Line 11 in App.tsx):**
```typescript
type Registration = { 
  _id: string; 
  fullName: string; 
  phone: string; 
  passportNumber: string; 
  date: string; 
  goDate: string; 
  backDate: string; 
  hotel?: string; 
  places?: string; 
  reference: string; 
  moneyAmount: number; 
  paid: boolean; 
  createdAt?: string 
}
```

**Form Field Handling:**
In the `RegistrationForm` component, the passport number is collected via:
```jsx
{field('passportNumber', 'Passport number')}
```
This creates an input field with the label "Passport number".

---

## 3. SIDEBAR STRUCTURE FOR BOTH DASHBOARDS

### Dashboard Detection
**Logic Location:** Line 26 in App.tsx
```typescript
const dashboard = authUser?.branch || 'hargeisa';
```
The `authUser` object contains a `branch` property that is either `'hargeisa'` or `'jidda'`.

---

### HARGEISA DASHBOARD SIDEBAR

**Location:** [frontend/src/App.tsx](frontend/src/App.tsx) - Lines 45-50 (approximately)

**Complete Sidebar JSX Structure:**
```jsx
<aside className={mobileNav ? 'sidebar open' : 'sidebar'}>
  
  {/* Brand Section */}
  <div className="brand">
    <span className="brand-mark">C</span>
    <div>
      <strong>Cabiir</strong>
      <small>Travel operations</small>
    </div>
    <button className="close-nav" onClick={() => setMobileNav(false)}>×</button>
  </div>

  {/* Manager Profile Section */}
  <div className="manager">
    <img 
      src={profile || `https://ui-avatars.com/api/?name=${encodeURIComponent(authUser.fullName)}&background=0b6e72&color=fff`} 
      alt={authUser.fullName} 
    />
    <div>
      <small>Signed in as</small>
      <strong>{authUser.fullName}</strong>
    </div>
    {/* HARGEISA ONLY - Upload Profile Button */}
    {dashboard === 'hargeisa' && 
      <label className="upload">
        Edit
        <input 
          type="file" 
          accept="image/*" 
          onChange={event => uploadProfile(event.target.files?.[0])} 
        />
      </label>
    }
  </div>

  {/* Overview Button */}
  <button 
    className={view === 'overview' ? 'nav-overview active' : 'nav-overview'} 
    onClick={() => setView('overview')}
  >
    ⌂ Overview
  </button>

  {/* HARGEISA ONLY - Create Record Section */}
  {dashboard === 'hargeisa' && <>
    <div className="nav-label form-label">Create record</div>
    
    {/* Create Registration Buttons */}
    {navItems.map(item => 
      <button 
        className="side-create" 
        key={item} 
        onClick={() => openForm(item)}
      >
        <span>＋</span>Register {labels[item]}
      </button>
    )}
    
    {/* Others Section Label */}
    <div className="nav-label other-label">Others</div>
    
    {/* Create Users Button */}
    <button 
      className="side-create" 
      onClick={() => { 
        setView('new-user'); 
        setUserForm(emptyUser); 
        setMobileNav(false) 
      }}
    >
      <span>＋</span>Create Users
    </button>
  </>}

  {/* Recycle Bin - Both Branches */}
  <button 
    className={view === 'recycle' ? 'side-create active' : 'side-create'} 
    onClick={() => { 
      setView('recycle'); 
      setMobileNav(false) 
    }}
  >
    <span>▣</span>Recycle Bin
  </button>

  {/* Workspace Navigation - Both Branches */}
  <div className="nav-label workspace-label">Workspace</div>
  <nav>
    {navItems.map(item => 
      <button 
        key={item} 
        className={view === item ? 'active' : ''} 
        onClick={() => { 
          setView(item); 
          setMobileNav(false) 
        }}
      >
        <span>
          {item === 'cumrah' ? '◈' : item === 'hajj' ? '✦' : '◌'}
        </span>
        {labels[item]} Registrations
      </button>
    )}
  </nav>

  {/* Footer */}
  <div className="sidebar-footer">
    <button onClick={logout}>
      <span>↪</span> Log out
    </button>
    <small>© 2026 Cabiir</small>
  </div>
</aside>
```

---

### JIDDA DASHBOARD SIDEBAR

**The Jidda sidebar is the same as Hargeisa EXCEPT:**

**Hidden/Removed Elements:**
1. ❌ No "Create record" section label
2. ❌ No "Register Cumrah" button
3. ❌ No "Register Hajj" button
4. ❌ No "Register Visitor" button
5. ❌ No "Others" section label
6. ❌ No "Create Users" button

**Visible Elements (Same as Hargeisa):**
- Brand section with logo
- Manager profile section (without Edit profile button)
- Overview button
- Recycle Bin button
- Workspace section with registration type navigation
- Footer with logout button

**CSS Styling Difference:**
The sidebar has different background gradient for Jidda:
```css
.jidda .sidebar { 
  background:linear-gradient(160deg,#243c62,#346696 70%,#527db0); 
}
```
(Hargeisa uses: `linear-gradient(160deg,#0d475b,#087d80 65%,#0b6b75)`)

---

### Sidebar Navigation Items

**Navigation items variable (Line ~48):**
```typescript
const navItems = ['cumrah', 'hajj', 'visitors'] as RegistrationType[]
```

**Labels mapping (Line 11):**
```typescript
const labels: Record<RegistrationType, string> = { 
  cumrah: 'Cumrah', 
  hajj: 'Hajj', 
  visitors: 'Visitor' 
}
```

**Icons for each type:**
- **Cumrah:** `◈`
- **Hajj:** `✦`
- **Visitors:** `◌`

---

## 4. BUTTONS/ACTIONS SPECIFIC TO REGISTRATION TYPES

### A. "Start New Registration" Actions

**Locations in Dashboard:**

#### 1. **Overview Quick Actions Section** (Line ~51)
**Component:** `Overview` function
```jsx
<div className="quick">
  <div>
    <span className="eyebrow">Quick actions</span>
    <h2>Start a new registration</h2>
  </div>
  {(['cumrah', 'hajj', 'visitors'] as RegistrationType[]).map(item => 
    <button key={item} onClick={() => openForm(item)}>
      <span>＋</span>
      <div>
        <strong>{labels[item]}</strong>
        <small>Add a new record</small>
      </div>
      <b>→</b>
    </button>
  )}
</div>
```
**Buttons Generated:**
- ＋ Cumrah (Add a new record)
- ＋ Hajj (Add a new record)
- ＋ Visitor (Add a new record)

#### 2. **Sidebar Create Record Buttons** (Line ~46-49, HARGEISA ONLY)
```jsx
{dashboard === 'hargeisa' && <>
  <div className="nav-label form-label">Create record</div>
  {navItems.map(item => 
    <button className="side-create" key={item} onClick={() => openForm(item)}>
      <span>＋</span>Register {labels[item]}
    </button>
  )}
</>}
```
**Buttons Generated (Hargeisa only):**
- ＋ Register Cumrah
- ＋ Register Hajj
- ＋ Register Visitor

---

### B. "Add [Type]" Actions in RegistrationTable

**Location:** `RegistrationTable` component (Line ~54)
```jsx
<button className="primary" onClick={() => openForm(type)}>
  ＋ Add {labels[type]}
</button>
```
**Buttons Generated (Appears for each registration type view):**
- ＋ Add Cumrah (shown when viewing Cumrah registrations)
- ＋ Add Hajj (shown when viewing Hajj registrations)
- ＋ Add Visitor (shown when viewing Visitor registrations)

---

### C. "Create Users" Action (HARGEISA ONLY)

**Location:** Sidebar "Others" section (Line ~49-50, HARGEISA ONLY)
```jsx
<button className="side-create" onClick={() => { 
  setView('new-user'); 
  setUserForm(emptyUser); 
  setMobileNav(false) 
}}>
  <span>＋</span>Create Users
</button>
```
**This button:**
- Creates a new Jidda user account
- Only appears in Hargeisa dashboard
- Opens the UserForm component

---

### D. Action Buttons in RegistrationTable Rows

**For each record, two action buttons:**
```jsx
<button className="action" onClick={() => openForm(type, record)}>
  Edit
</button>
<button className="action danger" onClick={() => remove(type, record._id)}>
  Delete
</button>
```

---

### E. Paid/Unpaid Checkbox

**In RegistrationTable:**
```jsx
<input 
  className="paid-checkbox" 
  type="checkbox" 
  checked={Boolean(record.paid)} 
  onChange={event => updatePaid(type, record._id, event.target.checked)} 
  aria-label={`Paid for ${record.fullName}`} 
/>
```
This toggles the payment status for each registration.

---

## 5. LOCATIONS WHERE REGISTRATION/ADD ACTIONS APPEAR IN JIDDA DASHBOARD

### Summary Table: Actions to Remove for Jidda Dashboard

| **Action** | **Location** | **Component** | **Line (approx)** | **Action Type** | **Status** |
|---|---|---|---|---|---|
| "＋ Register Cumrah" | Sidebar | App (main render) | ~46-49 | Conditional (Remove) | ❌ REMOVE |
| "＋ Register Hajj" | Sidebar | App (main render) | ~46-49 | Conditional (Remove) | ❌ REMOVE |
| "＋ Register Visitor" | Sidebar | App (main render) | ~46-49 | Conditional (Remove) | ❌ REMOVE |
| "＋ Create Users" | Sidebar | App (main render) | ~49-50 | Conditional (Remove) | ❌ REMOVE |
| "＋ Cumrah" (Quick action) | Overview Panel | Overview component | ~51 | Conditional (Remove) | ❌ REMOVE |
| "＋ Hajj" (Quick action) | Overview Panel | Overview component | ~51 | Conditional (Remove) | ❌ REMOVE |
| "＋ Visitor" (Quick action) | Overview Panel | Overview component | ~51 | Conditional (Remove) | ❌ REMOVE |
| "＋ Add Cumrah" (Header) | Table Header | RegistrationTable component | ~54 | Keep (Read-only) | ✅ KEEP |
| "＋ Add Hajj" (Header) | Table Header | RegistrationTable component | ~54 | Keep (Read-only) | ✅ KEEP |
| "＋ Add Visitor" (Header) | Table Header | RegistrationTable component | ~54 | Keep (Read-only) | ✅ KEEP |

---

### Detailed Removal Locations

#### **Location 1: Sidebar - Create Record Section (HARGEISA ONLY)**
**Current Code (Lines ~46-49):**
```jsx
{dashboard === 'hargeisa' && <>
  <div className="nav-label form-label">Create record</div>
  {navItems.map(item => 
    <button className="side-create" key={item} onClick={() => openForm(item)}>
      <span>＋</span>Register {labels[item]}
    </button>
  )}
```
**Action:** Already conditional! Already hidden for Jidda.

---

#### **Location 2: Sidebar - Create Users Button (HARGEISA ONLY)**
**Current Code (Lines ~49-56):**
```jsx
  <div className="nav-label other-label">Others</div>
  <button className="side-create" onClick={() => { 
    setView('new-user'); 
    setUserForm(emptyUser); 
    setMobileNav(false) 
  }}>
    <span>＋</span>Create Users
  </button>
</>}
```
**Action:** Already conditional! Already hidden for Jidda.

---

#### **Location 3: Overview Panel - Quick Actions (NEEDS CONDITIONAL)**
**Current Code (Line ~51):**
```jsx
function Overview({ stats, dashboard, openForm }: { stats: Stats; dashboard: string; openForm: (type: RegistrationType) => void }) { 
  const metric = (type: RegistrationType) => stats.byType.find(item => item.type === type)?.count || 0; 
  return (
    <section className="content">
      <div className="welcome">
        <div>
          <span className="eyebrow">{dashboard} office</span>
          <h2>Operations at a glance</h2>
          <p>Live totals from the shared MongoDB workspace.</p>
        </div>
        <div className="welcome-orb">✈</div>
      </div>
      <div className="stat-grid overview-grid">
        {/* Stats cards... */}
      </div>
      {/* THIS SECTION NEEDS TO BE CONDITIONAL */}
      <div className="quick">
        <div>
          <span className="eyebrow">Quick actions</span>
          <h2>Start a new registration</h2>
        </div>
        {(['cumrah', 'hajj', 'visitors'] as RegistrationType[]).map(item => 
          <button key={item} onClick={() => openForm(item)}>
            <span>＋</span>
            <div>
              <strong>{labels[item]}</strong>
              <small>Add a new record</small>
            </div>
            <b>→</b>
          </button>
        )}
      </div>
    </section>
  )
}
```

**Recommended Fix:** Wrap the entire `<div className="quick">` section with a conditional:
```jsx
{dashboard === 'hargeisa' && (
  <div className="quick">
    {/* quick actions content */}
  </div>
)}
```

---

### Summary: Already Protected vs Needs Protection

**✅ Already Protected (Conditional on `dashboard === 'hargeisa'`):**
1. Create Record sidebar buttons (Register Cumrah, Hajj, Visitor)
2. Create Users button

**⚠️ NEEDS PROTECTION (Currently visible for all branches):**
1. Overview Quick Actions section - Shows 3 registration buttons to all users
   - Should be conditional: `{dashboard === 'hargeisa' && <div className="quick">...`

---

## COMPLETE FILE REFERENCE

| Component | File | Lines | Type |
|---|---|---|---|
| RegistrationTable | [frontend/src/App.tsx](frontend/src/App.tsx) | ~54 | Function |
| Overview | [frontend/src/App.tsx](frontend/src/App.tsx) | ~51 | Function |
| Sidebar (Main render) | [frontend/src/App.tsx](frontend/src/App.tsx) | ~45-50 | JSX in main return |
| RegistrationForm | [frontend/src/App.tsx](frontend/src/App.tsx) | ~53 | Function |
| UserForm | [frontend/src/App.tsx](frontend/src/App.tsx) | ~53 | Function |
| App (main) | [frontend/src/App.tsx](frontend/src/App.tsx) | Line 17 | Function |

---

## KEY CONFIGURATION VARIABLES

**Line 8:** Registration Types
```typescript
type RegistrationType = 'cumrah' | 'hajj' | 'visitors'
```

**Line 11:** Type Labels
```typescript
const labels: Record<RegistrationType, string> = { cumrah: 'Cumrah', hajj: 'Hajj', visitors: 'Visitor' }
```

**Line 11:** Registration Form Fields
```typescript
const emptyForm = { fullName: '', phone: '', passportNumber: '', date: '', goDate: '', backDate: '', hotel: '', places: '', reference: '', moneyAmount: '' }
```

**Authentication:**
- Token stored in `localStorage` as `'cabiir-token'`
- User stored in `localStorage` as `'cabiir-user'`
- User branch retrieved via `authUser?.branch`

---

## COLOR SCHEME

**Hargeisa Dashboard:**
- Gradient: `linear-gradient(160deg,#0d475b,#087d80 65%,#0b6b75)`
- Primary: `#087c80` (Teal)

**Jidda Dashboard:**
- Gradient: `linear-gradient(160deg,#243c62,#346696 70%,#527db0)`
- Primary: `#346696` (Navy Blue)

---
