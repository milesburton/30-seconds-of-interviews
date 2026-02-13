# Security Policy

## ⚠️ Legacy Repository Notice

**This repository is LEGACY/UNMAINTAINED and contains known security vulnerabilities that cannot be easily resolved.**

This is a **fork** of a community documentation project (interview questions) that is no longer actively maintained.

### Known Critical Security Issues

This repository has **7 CRITICAL** and **10 HIGH** security vulnerabilities:

**Critical:**
1. **elliptic** (x2) - Private key extraction in ECDSA signatures
2. **babel-traverse** - Arbitrary code execution (NO PATCH AVAILABLE)
3. **cryptiles** - Insufficient entropy in cryptographic operations
4. **fsevents** - Code injection vulnerability
5. **minimist** (x2) - Prototype pollution attacks

**High:**
- Multiple ReDoS (Regular Expression Denial of Service) vulnerabilities
- Cross-spawn, braces, hoek, tar, browserify-sign issues
- HTTP cache semantics vulnerability

### Why Can't These Be Fixed?

- Uses **Babel 6.x** ecosystem which is no longer maintained
- babel-traverse vulnerability has **no patch available** - would require complete rewrite to Babel 7+
- **npm is listed as a dependency** (highly unusual and problematic)
- Complex web of transitive dependencies from 2017-2018
- Parcel bundler v1.x is deprecated
- Fixing these issues would require a complete rebuild with modern tooling

### Context

This is a **forked documentation website** containing common interview questions. It is:
- Not a production application
- Used for static documentation only
- Originally from https://github.com/Chalarangelo/30-seconds-of-interviews
- Last meaningfully updated in 2018-2019

### Recommendations

**For Users:**
- ❌ **DO NOT** clone and run this repository
- ❌ **DO NOT** use for any production purpose
- ✅ Visit the **original upstream repository** for maintained content
- ✅ View the static site at https://30secondsofinterviews.org/ if still available

**For Maintainers:**
- Consider archiving this fork if not actively maintained
- If maintenance is desired, complete rewrite needed with:
  - Modern build tools (Vite, Next.js, Astro, etc.)
  - Current dependencies (Babel 7+, or drop Babel entirely)
  - Updated React/Parcel versions

### Reporting Security Issues

As this is an unmaintained legacy fork, security reports will not be actively addressed. If you need this content:
1. Visit the original upstream repository
2. Create a modern fork with updated dependencies
3. Use this only as historical reference

---

**Original Repository:** https://github.com/Chalarangelo/30-seconds-of-interviews  
**Fork Created:** ~2018-2019  
**Status:** LEGACY/UNMAINTAINED FORK  
**Last Updated:** 2026-02-13  
**Vulnerability Count:** 7 CRITICAL, 10 HIGH, Multiple MEDIUM/LOW
