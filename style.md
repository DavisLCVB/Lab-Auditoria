# Guía de Estilo Unificado 2026 - Universidad Nacional

## Visión
Sistema de diseño moderno, vistoso y cohesivo para todos los aplicativos institucionales (`SUM-clone-w-vulns`, `Gestion-certificados-Auditoria`, `tramite-legacy`).

## Identidad visual
- **Tono**: Profesional con personalidad moderna.
- **Sensación**: Interfaces limpias con detalles de color vibrantes.
- **Diferenciador**: Gradientes suaves, transiciones fluidas, microinteracciones.

## Tipografías
| Uso            | Familia                                                  |
|----------------|----------------------------------------------------------|
| UI Principal   | `Inter`, -apple-system, BlinkMacSystemFont, sans-serif   |
| Encabezados    | `DM Serif Display`, Georgia, serif                       |
| Terminal/Código| `JetBrains Mono`, `Fira Code`, `Courier New`, monospace |

## Paleta de Tokens CSS
```css
:root {
  /* Fondos */
  --bg: #f0f4f8;
  --surface: #ffffff;
  
  /* Marca principal (grises azulados) */
  --brand-900: #0f172a;
  --brand-800: #1e293b;
  --brand-700: #334155;
  --brand-600: #475569;
  --brand-500: #64748b;
  
  /* Acentos de color */
  --accent-gold: #f59e0b;
  --accent-amber: #d97706;
  --accent-emerald: #10b981;
  --accent-sky: #0ea5e9;
  --accent-violet: #8b5cf6;
  
  /* Utilidad */
  --muted: #64748b;
  --line: #e2e8f0;
  --ok: #22c55e;
  --warn: #eab308;
  --danger: #ef4444;
  
  /* Sombras */
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.05);
  --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
}
```

## Gradientes principales
```css
/* Navbar y cabeceras */
background: linear-gradient(135deg, var(--brand-900), var(--brand-800) 50%, var(--brand-700));

/* Acento decorativo (línea superior de cards) */
background: linear-gradient(90deg, var(--accent-sky), var(--accent-violet));

/* Botones admin */
background: linear-gradient(135deg, #fbbf24 0%, #f59e0b 100%);

/* Login fondos */
background: linear-gradient(135deg, #0f172a, #1e293b 40%, #334155);
```

## Componentes

### Navegación (.nav-shell)
- Gradiente 135° de brand-900 a brand-700
- Sombra prominente (0 4px 20px)
- Border-bottom sutil con transparencia

### Cards (.card, .kpi-card, .section-card)
- Border-radius: 16px
- Transición hover: elevación + translateY(-2px)
- KPI cards: línea decorativa superior con gradiente sky→violet
- Section cards: cabecera con gradiente de marca

### Tablas (.table-modern)
- Headers con gradiente vertical sutil
- Hover de rows con gradiente horizontal translúcido
- Padding generoso (14px 16px)

### Formularios
- Inputs con borde 2px, radius 10px
- Focus: borde sky + box-shadow con glow
- Botones con sombra y hover elevado

### Login
- Fondo con gradientes radiales decorativos
- Card con border-radius 24px
- Sombra XL + glow sutil

## Layout responsive
- **Dashboard**: Grid de KPIs (auto-fit, minmax 260px)
- **Contenido**: max-width 1100px, padding 24px
- **Espaciado**: mb-4 / py-4 entre bloques

## Microinteracciones
- Transiciones: 0.2s - 0.3s ease
- Hover en cards: elevación + translateY(-2px)
- Hover en botones: translateY(-1px) + sombra más profunda

## Bootstrap incluido
- Versión: 5.3.2
- Icons: Bootstrap Icons (CDN)

## Checklist de adopción
- [ ] Importar fuentes (Inter + DM Serif Display + JetBrains Mono)
- [ ] Copiar tokens :root
- [ ] Aplicar gradiente a navegación
- [ ] Usar clases unificadas (kpi-card, section-card, table-modern)
- [ ] Incluir línea decorativa en cards importantes
- [ ] Validar hover states y transiciones
- [ ] Probar en viewport móvil
