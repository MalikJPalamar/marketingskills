# Schema Markup — Centaurion.me
*April 2026 · Skill: schema-markup · Author: Malik Palamar*

---

## Schema Coverage Map

| Page / Section | Schema Types | Rich Result Target | Priority |
|---|---|---|---|
| Homepage | `Organization`, `WebSite`, `Person` | Sitelinks search box, entity panel | P0 |
| Methodology hub | `Article`, `BreadcrumbList` | Article rich result | P0 |
| Blog posts | `BlogPosting`, `BreadcrumbList` | Article rich result | P0 |
| Glossary terms | `DefinedTerm`, `FAQPage` | FAQ rich result | P1 |
| Work With Us / Service pages | `Service`, `FAQPage` | FAQ rich result | P1 |
| Case Studies | `Article`, `BreadcrumbList` | Article rich result | P1 |
| Agentic Engineering levels | `Article`, `HowTo` (Levels 1-8) | HowTo rich result | P2 |
| About / Malik Palamar | `Person`, `BreadcrumbList` | Knowledge panel | P2 |
| All pages with breadcrumbs | `BreadcrumbList` | Breadcrumb SERP display | P0 |

---

## JSON-LD Implementations

### 1. Homepage — Organization + WebSite + Person

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://centaurion.me/#organization",
      "name": "Centaurion",
      "url": "https://centaurion.me",
      "logo": {
        "@type": "ImageObject",
        "url": "https://centaurion.me/images/centaurion-logo.png",
        "width": 200,
        "height": 60
      },
      "description": "Human-AI augmentation advisory framework. Engineering methodology for building cognitive composites where humans remain the most important variable.",
      "foundingDate": "2025",
      "founder": {
        "@id": "https://centaurion.me/about/malik-palamar/#person"
      },
      "sameAs": [
        "https://github.com/MalikJPalamar",
        "https://linkedin.com/in/malikpalamar",
        "https://centaurion.me"
      ],
      "knowsAbout": [
        "Agentic Engineering",
        "Human-AI Augmentation",
        "AI Transformation",
        "Free Energy Principle",
        "Active Inference"
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://centaurion.me/#website",
      "url": "https://centaurion.me",
      "name": "Centaurion",
      "description": "Human-AI augmentation advisory. The engineering methodology for building cognitive composites.",
      "publisher": {
        "@id": "https://centaurion.me/#organization"
      },
      "potentialAction": {
        "@type": "SearchAction",
        "target": {
          "@type": "EntryPoint",
          "urlTemplate": "https://centaurion.me/search?q={search_term_string}"
        },
        "query-input": "required name=search_term_string"
      }
    },
    {
      "@type": "Person",
      "@id": "https://centaurion.me/about/malik-palamar/#person",
      "name": "Malik Palamar",
      "url": "https://centaurion.me/about/malik-palamar",
      "jobTitle": "Fractional CEO & Chief AI Officer",
      "worksFor": {
        "@id": "https://centaurion.me/#organization"
      },
      "description": "Systems engineer and Chief AI Officer. Creator of the Centaurion Method and the 11 Levels of Agentic Engineering framework.",
      "sameAs": [
        "https://github.com/MalikJPalamar",
        "https://linkedin.com/in/malikpalamar"
      ],
      "knowsAbout": [
        "Agentic Engineering",
        "AI Transformation",
        "Free Energy Principle",
        "Human-AI Augmentation",
        "Systems Engineering"
      ]
    }
  ]
}
```

---

### 2. Blog Post / Article Template

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "BlogPosting",
      "@id": "https://centaurion.me/blog/[post-slug]/#article",
      "headline": "[Post Title — max 110 chars]",
      "description": "[150-160 char meta description]",
      "image": {
        "@type": "ImageObject",
        "url": "https://centaurion.me/images/blog/[post-slug]-og.png",
        "width": 1200,
        "height": 630
      },
      "datePublished": "[YYYY-MM-DD]",
      "dateModified": "[YYYY-MM-DD]",
      "author": {
        "@id": "https://centaurion.me/about/malik-palamar/#person"
      },
      "publisher": {
        "@id": "https://centaurion.me/#organization"
      },
      "mainEntityOfPage": {
        "@type": "WebPage",
        "@id": "https://centaurion.me/blog/[post-slug]"
      },
      "keywords": "[comma-separated keywords]",
      "articleSection": "[Methodology | Agentic Engineering | AI Strategy | Case Studies]",
      "wordCount": "[approximate word count]",
      "isPartOf": {
        "@id": "https://centaurion.me/#website"
      }
    },
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://centaurion.me"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Blog",
          "item": "https://centaurion.me/blog"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "[Post Title]",
          "item": "https://centaurion.me/blog/[post-slug]"
        }
      ]
    }
  ]
}
```

---

### 3. Glossary Term — DefinedTerm + FAQPage

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "DefinedTerm",
      "@id": "https://centaurion.me/glossary/[term-slug]/#term",
      "name": "[Term Name]",
      "description": "[One-sentence definition]",
      "inDefinedTermSet": {
        "@type": "DefinedTermSet",
        "name": "Centaurion Glossary",
        "url": "https://centaurion.me/glossary"
      },
      "url": "https://centaurion.me/glossary/[term-slug]"
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is [term]?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "[40-60 word definition. Self-contained answer. Should work without surrounding context.]"
          }
        },
        {
          "@type": "Question",
          "name": "How does [term] apply to AI systems?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "[40-60 word application-focused answer. Reference Centaurion framework where relevant.]"
          }
        },
        {
          "@type": "Question",
          "name": "Why does [term] matter for organizations?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "[40-60 word business-context answer. Connect to prediction error, fitness, or closed-loop concepts.]"
          }
        }
      ]
    },
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://centaurion.me"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Glossary",
          "item": "https://centaurion.me/glossary"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "[Term Name]",
          "item": "https://centaurion.me/glossary/[term-slug]"
        }
      ]
    }
  ]
}
```

---

### 4. Agentic Engineering Level Page — HowTo

*(Apply to Levels 1–8 which are implementable practices. Levels 9–11 use Article schema.)*

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "HowTo",
      "@id": "https://centaurion.me/agentic-engineering/level-[n]-[slug]/#howto",
      "name": "How to reach Level [N]: [Level Name] in Agentic Engineering",
      "description": "[One-sentence description of what this level achieves]",
      "totalTime": "PT[X]H",
      "tool": [
        {
          "@type": "HowToTool",
          "name": "[Primary tool/platform]"
        }
      ],
      "step": [
        {
          "@type": "HowToStep",
          "position": 1,
          "name": "[Step name]",
          "text": "[Step description — 40-80 words]",
          "url": "https://centaurion.me/agentic-engineering/level-[n]-[slug]/#step-1"
        }
      ],
      "author": {
        "@id": "https://centaurion.me/about/malik-palamar/#person"
      }
    },
    {
      "@type": "Article",
      "headline": "Level [N]: [Level Name] — The 11 Levels of Agentic Engineering",
      "datePublished": "[YYYY-MM-DD]",
      "dateModified": "[YYYY-MM-DD]",
      "author": {
        "@id": "https://centaurion.me/about/malik-palamar/#person"
      },
      "publisher": {
        "@id": "https://centaurion.me/#organization"
      }
    },
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://centaurion.me"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Agentic Engineering",
          "item": "https://centaurion.me/agentic-engineering"
        },
        {
          "@type": "ListItem",
          "position": 3,
          "name": "Level [N]: [Level Name]",
          "item": "https://centaurion.me/agentic-engineering/level-[n]-[slug]"
        }
      ]
    }
  ]
}
```

---

### 5. Work With Us / Service Page

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Service",
      "@id": "https://centaurion.me/work-with-us/[service-slug]/#service",
      "name": "[Service Name]",
      "description": "[Service description — 100-150 words]",
      "provider": {
        "@id": "https://centaurion.me/#organization"
      },
      "serviceType": "[Fractional CAO | AI Transformation Advisory | Workshops]",
      "audience": {
        "@type": "Audience",
        "audienceType": "Mid-market organizations, technical leaders, C-suite executives"
      },
      "areaServed": "Worldwide",
      "url": "https://centaurion.me/work-with-us/[service-slug]"
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is a Fractional Chief AI Officer?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "A Fractional CAO is a part-time Chief AI Officer who provides strategic AI leadership to organizations that need executive-level AI expertise without a full-time hire. They define AI strategy, govern AI adoption, and ensure human primacy in AI system design."
          }
        },
        {
          "@type": "Question",
          "name": "Who is the Fractional CAO engagement for?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Mid-market organizations (sub-$50M revenue) undergoing AI transformation who need methodology and governance, not just tool implementation. Ideal for founders and executives navigating their first serious AI adoption cycle."
          }
        },
        {
          "@type": "Question",
          "name": "How long does an AI transformation engagement take?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Engagements typically start with a 30-day pilot audit (systems map, AI readiness assessment, quick wins), followed by a 90-day implementation phase. Full transformation programs run 6-12 months depending on organizational complexity."
          }
        }
      ]
    }
  ]
}
```

---

### 6. Methodology Hub Page

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Article",
      "@id": "https://centaurion.me/methodology/#article",
      "headline": "The Centaurion Method: Human-AI Augmentation Framework",
      "description": "The Centaurion Method is a scientific framework for building human-AI composite systems grounded in Karl Friston's Free Energy Principle. It includes Three Laws, a Fitness Equation, and Five Sensing Layers.",
      "image": "https://centaurion.me/images/methodology-og.png",
      "datePublished": "2026-04-01",
      "dateModified": "2026-04-01",
      "author": {
        "@id": "https://centaurion.me/about/malik-palamar/#person"
      },
      "publisher": {
        "@id": "https://centaurion.me/#organization"
      },
      "mainEntityOfPage": "https://centaurion.me/methodology",
      "about": [
        {
          "@type": "Thing",
          "name": "Free Energy Principle",
          "sameAs": "https://en.wikipedia.org/wiki/Free_energy_principle"
        },
        {
          "@type": "Thing",
          "name": "Active Inference",
          "sameAs": "https://en.wikipedia.org/wiki/Active_inference"
        },
        {
          "@type": "Thing",
          "name": "Human-AI Collaboration"
        }
      ]
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is the Centaurion Method?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "The Centaurion Method is a human-AI augmentation framework grounded in Karl Friston's Free Energy Principle. It states that the fitness of any cognitive system equals predictive order divided by thermodynamic cost (-ε/C), and provides Three Laws, Five Sensing Layers, and an active inference loop for implementation."
          }
        },
        {
          "@type": "Question",
          "name": "What are the Three Laws of Centaurion?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "The Three Laws are: (1) The Hierarchy Law — the human is the prior, not the bottleneck; (2) The Routing Law — prediction errors are routed to the correct substrate (routine to AI, novel to humans); (3) The Coupling Law — the exo-cortex maintains shared model state between human and AI."
          }
        },
        {
          "@type": "Question",
          "name": "How is Centaurion different from other AI consulting frameworks?",
          "acceptedAnswer": {
            "@type": "Answer",
            "text": "Centaurion is grounded in a falsifiable scientific model (Friston's Free Energy Principle) with measurable prediction error metrics. It closes the feedback loop most implementations ignore, and treats the exo-cortex as both a product and proof of concept — built in production, not theorized about."
          }
        }
      ]
    },
    {
      "@type": "BreadcrumbList",
      "itemListElement": [
        {
          "@type": "ListItem",
          "position": 1,
          "name": "Home",
          "item": "https://centaurion.me"
        },
        {
          "@type": "ListItem",
          "position": 2,
          "name": "Methodology",
          "item": "https://centaurion.me/methodology"
        }
      ]
    }
  ]
}
```

---

## WordPress Implementation Notes

If centaurion.me is running WordPress:

1. **Rank Math** (recommended): Supports `DefinedTerm`, `Service`, `Person`, and custom schema types. Add custom JSON-LD via Rank Math → Schema → Custom Schema.
2. **Yoast SEO**: Add custom schema via `wpseo_schema_graph` filter in `functions.php`.
3. **Manual injection**: Add JSON-LD blocks via a `<script>` tag in the page template or via a custom block.

For non-WordPress (custom/static site): inject JSON-LD in the `<head>` of each page template. Use page-type variables to populate dynamic fields (headline, datePublished, breadcrumb items).

---

## Validation Checklist

For every new page before publishing:
- [ ] Run through [Google Rich Results Test](https://search.google.com/test/rich-results)
- [ ] Zero errors (warnings acceptable)
- [ ] Schema content matches visible page content
- [ ] All `@id` values use absolute URLs
- [ ] `datePublished` and `dateModified` in ISO 8601 format (YYYY-MM-DD)
- [ ] Author `@id` matches the canonical Person node
- [ ] BreadcrumbList matches actual URL hierarchy
- [ ] After publishing: check Search Console > Enhancements in 48 hours
