# RuVNet Portfolio - Complete Documentation

> Your cutting-edge portfolio site for showcasing AI-generated web projects and landing local web development work

## 📚 Documentation

This repository includes everything you need to get your portfolio running and deploy your v0 projects:

### Getting Started
- **[SETUP.md](./SETUP.md)** - Complete setup guide (prerequisites, installation, environment variables, local development)
- **[README.md](./README.md)** - Project overview and quick reference

### Deployment & Operations
- **[DEPLOYMENT.md](./DEPLOYMENT.md)** - How to deploy to GitHub Pages with GitHub Actions
- **[V0_AUDIT_GUIDE.md](./V0_AUDIT_GUIDE.md)** - How to prepare and deploy your v0 projects

### Customization
- **[CUSTOMIZE.md](./CUSTOMIZE.md)** - How to customize colors, sections, and branding

---

## 🚀 Quick Start (5 Minutes)

### 1. Clone Repository
```bash
git clone https://github.com/jasonclarkagain/ruvnet-portfolio.git
cd ruvnet-portfolio
```

### 2. Install Dependencies
```bash
# Using Bun (recommended - faster)
bun install

# Or using npm
npm install
```

### 3. Set Up Environment
```bash
# Copy environment template
cp .env.example .env.local

# Edit .env.local and add:
# - Your GitHub username
# - GitHub personal access token (from github.com/settings/tokens)
# - Your email for contact form
# - Formspree form ID (from formspree.io)
```

### 4. Run Locally
```bash
bun run dev
```
Open [http://localhost:3000](http://localhost:3000)

### 5. Deploy to GitHub Pages
```bash
git add .
git commit -m "Deploy portfolio"
git push origin main
```

**Your site goes live at:** `https://jasonclarkagain.github.io/ruvnet-portfolio`

---

## ⚡ Tech Stack

| Technology | Purpose |
|-----------|----------|
| **Next.js 15** | React framework |
| **React 19** | UI library |
| **TypeScript** | Type safety |
| **Tailwind CSS** | Styling |
| **Bun** | JavaScript runtime |
| **GitHub Pages** | Hosting |
| **GitHub Actions** | CI/CD |
| **Formspree** | Contact form (free) |

---

## 📁 What's Included

### Components
- ✅ Responsive header with navigation
- ✅ Hero section with CTAs
- ✅ About/bio section with tech stack
- ✅ Projects section (auto-fetches GitHub repos)
- ✅ Services section (customize what you offer)
- ✅ Contact form with validation
- ✅ Footer with links

### Features
- ✅ Dark theme with custom accent colors
- ✅ Smooth animations and transitions
- ✅ Mobile responsive design
- ✅ GitHub API integration
- ✅ SEO optimized (meta tags, sitemap, robots.txt)
- ✅ Automatic GitHub Pages deployment
- ✅ Free contact form (Formspree)

---

## 🎯 Your Workflow

### Phase 1: Local Development
1. Clone repo
2. Install dependencies
3. Configure environment variables
4. Run `bun run dev`
5. Customize content, colors, sections
6. Test locally

### Phase 2: Prepare v0 Projects
1. Read [V0_AUDIT_GUIDE.md](./V0_AUDIT_GUIDE.md)
2. Check each v0 project for missing files
3. Add `.gitignore`, `.env.example`, README
4. Test build locally (`bun run build`)
5. Choose top 5-10 to showcase

### Phase 3: Deploy
1. Push portfolio to main branch
2. GitHub Actions automatically builds
3. Site goes live on GitHub Pages
4. Deploy best v0 projects to GitHub Pages or Vercel
5. Link them from portfolio

### Phase 4: Market Locally
1. Add your local area info
2. Share portfolio URL
3. Update GitHub profile bio
4. Link from v0 projects back to portfolio
5. Get local clients!

---

## 📖 Command Reference

```bash
# Development
bun run dev              # Start local dev server

# Production
bun run build            # Create optimized build
bun run start            # Run production build

# Linting
bun run lint             # Check code quality

# Deployment
git push origin main     # Trigger GitHub Actions

# Clean up
rm -rf node_modules      # Remove dependencies
rm -rf .next             # Remove build cache
```

---

## 🎨 Customization Examples

### Change Site Title
**File:** `.env.local`
```bash
NEXT_PUBLIC_SITE_TITLE=Jason Clark - Web Developer
NEXT_PUBLIC_AUTHOR_EMAIL=your-email@example.com
```

### Change Colors
**File:** `tailwind.config.ts`
```typescript
colors: {
  'accent': '#00d9ff',           // Change to your color
  'accent-secondary': '#ff006e',  // Change to your color
}
```

### Update Your Bio
**File:** `components/sections/About.tsx`
```tsx
<p className="text-lg text-gray-300 mb-6">
  I'm a developer who loves building with cutting-edge tech.
  {/* Your custom bio here */}
</p>
```

### Add Services
**File:** `components/sections/Services.tsx`
```typescript
const services = [
  {
    title: 'Your Service',
    description: 'Description of what you offer',
    icon: '🚀',
  },
  // Add more services
];
```

See [CUSTOMIZE.md](./CUSTOMIZE.md) for more examples.

---

## ✅ Pre-Launch Checklist

- [ ] `.env.local` configured with your GitHub token and Formspree ID
- [ ] Site loads at `http://localhost:3000`
- [ ] All navigation links work
- [ ] Projects section shows your GitHub repos
- [ ] Contact form submits without errors
- [ ] Mobile responsive (test on phone)
- [ ] No console errors in browser DevTools
- [ ] `bun run build` completes successfully
- [ ] Deployed to GitHub Pages
- [ ] Live site accessible at your GitHub Pages URL

---

## 🆘 Troubleshooting

### Site won't load locally
```bash
# Check if port 3000 is in use
# Kill any process on port 3000
# Clear cache
rm -rf .next
# Reinstall dependencies
rm -rf node_modules
bun install
# Try again
bun run dev
```

### GitHub API not loading projects
- Check `.env.local` has `NEXT_PUBLIC_GITHUB_ORG` and `NEXT_PUBLIC_GITHUB_TOKEN`
- Verify GitHub token is valid: https://github.com/settings/tokens
- Check GitHub API isn't rate-limited (60 requests/hour for unauthenticated)

### Contact form not working
- Go to [formspree.io](https://formspree.io) and create a form
- Copy the form ID (e.g., `f_abc123`)
- Update `components/sections/Contact.tsx` with your form ID
- Test the form

### Deployment not triggering
- Check `.github/workflows/deploy.yml` exists
- Go to repo **Actions** tab
- Look for "Deploy to GitHub Pages" workflow
- If failed, click to see error logs
- Push a new commit to trigger again

---

## 📚 Additional Resources

### Documentation
- [Next.js Docs](https://nextjs.org/docs)
- [Tailwind CSS](https://tailwindcss.com/docs)
- [React Docs](https://react.dev)
- [TypeScript](https://www.typescriptlang.org/docs)
- [Bun Runtime](https://bun.sh/docs)

### Tools & Services (All Free)
- [GitHub Pages](https://pages.github.com) - Hosting
- [GitHub Actions](https://github.com/features/actions) - CI/CD
- [Formspree](https://formspree.io) - Contact forms
- [GitHub API](https://docs.github.com/en/rest) - Project data

### Deployment
- [GitHub Pages Deploy Guide](./DEPLOYMENT.md)
- [v0 Projects Audit Guide](./V0_AUDIT_GUIDE.md)

---

## 🔮 Future Enhancements

Phase ideas for future development:

### Phase 1: Interactive
- [ ] Add Three.js 3D scene
- [ ] Animated hero section
- [ ] Scroll-based animations

### Phase 2: Backend
- [ ] Rust API backend
- [ ] Go microservices
- [ ] Database integration

### Phase 3: Content
- [ ] Blog/case studies
- [ ] Client testimonials
- [ ] Project case studies
- [ ] Newsletter signup

### Phase 4: Marketing
- [ ] Google Analytics
- [ ] SEO optimization
- [ ] Social media cards
- [ ] Custom domain

---

## 💡 Pro Tips

1. **Keep it updated** - Push changes regularly to keep portfolio fresh
2. **Showcase your best** - Link your 5-10 best v0 projects prominently
3. **Document everything** - Good README = more trust from clients
4. **Test on mobile** - Most people view on phones
5. **Use your local angle** - Mention your area to attract local clients
6. **Add testimonials** - Even one client quote boosts credibility
7. **Keep portfolio simple** - Don't overload with too many projects
8. **Update GitHub** - Keep contributing to show you're active

---

## 📝 License

MIT License - Use freely for your portfolio!

---

## 🤝 Support

**Questions or issues?**

1. Check the relevant guide:
   - Setup issues → [SETUP.md](./SETUP.md)
   - Deployment issues → [DEPLOYMENT.md](./DEPLOYMENT.md)
   - Customization → [CUSTOMIZE.md](./CUSTOMIZE.md)
   - v0 projects → [V0_AUDIT_GUIDE.md](./V0_AUDIT_GUIDE.md)

2. Check GitHub:
   - Open an issue
   - Search closed issues
   - Check Actions logs

3. Next.js docs:
   - [nextjs.org/docs](https://nextjs.org/docs)

---

## ⭐ Built With These Technologies

```
┌─────────────────────────────────────┐
│                                     │
│  Next.js 15 + React 19 + TypeScript │
│       Tailwind CSS + Bun Runtime    │
│   GitHub Pages + GitHub Actions     │
│         + Formspree + GitHub API    │
│                                     │
│     Building the Cutting Edge       │
│        Locally, For Local Work      │
│                                     │
└─────────────────────────────────────┘
```

---

**Ready to launch your portfolio? Start with [SETUP.md](./SETUP.md)! 🚀**

**Want to deploy your v0 projects? Read [V0_AUDIT_GUIDE.md](./V0_AUDIT_GUIDE.md)! 📦**
