# [GitHub ReadMe Stats](https://github.com/anuraghazra/github-readme-stats "GitHub Readme Stats")

## Documentación: Personalización de Tarjetas de GitHub Stats

GitHub Stats es una herramienta que permite generar tarjetas dinámicas con estadísticas de perfil de GitHub.

---

### **1. Tarjeta Básica**

Para generar una tarjeta con las estadísticas básicas:

```markdown
[![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay)](https://github.com/anuraghazra/github-readme-stats)
```

[![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay)](https://github.com/anuraghazra/github-readme-stats)

---

### **2. Ocultar Estadísticas Individuales**

Puedes ocultar ciertas métricas utilizando el parámetro `&hide=`.

- Opciones: `stars, commits, prs, issues, contribs`

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&hide=contribs,prs)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&hide=contribs,prs)

---

### **3. Mostrar Estadísticas Adicionales**

Utiliza el parámetro `&show=` para incluir métricas adicionales.

- Opciones: `reviews, discussions_started, discussions_answered, prs_merged, prs_merged_percentage`

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&show=reviews,prs_merged,prs_merged_percentage)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&show=reviews,prs_merged,prs_merged_percentage)

---

### **4. Mostrar Iconos**

Activa los iconos añadiendo `&show_icons=true`.

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&show_icons=true)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&show_icons=true)

---

### **5. Temas**

Personaliza los colores de la tarjeta con temas predefinidos:

- Temas disponibles: `dark, radical, merko, gruvbox, tokyonight, onedark, cobalt, synthwave, highcontrast, dracula`

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&theme=radical&show_icons=true)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&theme=radical&show_icons=true)

### **6. Fondo Transparente**

Para un fondo transparente, usa `&theme=transparent` o ajusta el color de fondo con el parámetro `&bg_color=00000000`.

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&theme=transparent)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&theme=transparent)

---

### **7. Colores Personalizados**

Cambia colores específicos con los parámetros:

- `title_color`: Color del título.
- `text_color`: Color del texto.
- `icon_color`: Color de los iconos.
- `bg_color`: Color de fondo (soporta gradientes).

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&title_color=ff5733&text_color=ffffff&icon_color=00ff00&bg_color=45,000000,1e90ff)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&title_color=ff5733&text_color=ffffff&icon_color=00ff00&bg_color=45,000000,1e90ff)

---

### **8. Cambiar el Idioma**

Puedes cambiar el idioma con el parámetro `&locale=`.

- Idiomas disponibles: `es, en, fr, pt-br, ja`, entre otros.

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&locale=es)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&locale=es)

---

### **9. Opciones Avanzadas**

- **Sin bordes:** `&hide_border=true`
- **Título personalizado:** `&custom_title=Estadísticas Josuesay`
- **Formato de números:** `&number_format=long`
- **Ancho de tarjeta:** `&card_width=600`
- **Altura de líneas:** `&line_height=30`

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&hide_border=true&custom_title=Estadísticas%20Josuesay&line_height=30)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&hide_border=true&custom_title=Estadísticas%20Josuesay&line_height=30)

### **10. Tipos de Rango**

Puedes personalizar cómo se muestra el rango en tu tarjeta utilizando el parámetro `rank_icon=`.

- **Opciones disponibles**:
  - `default`: Muestra letras (A+, A, B+, etc.).
  - `github`: Muestra el logo de GitHub.
  - `none`: Oculta el rango.

```markdown
![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&rank_icon=github)
```

![Estadísticas de GitHub](https://github-readme-stats.vercel.app/api?username=josuesay&rank_icon=github)

## Documentación: Personalización de Tarjetas de GitHub Stats (Top Languages Card

Las estadísticas de lenguajes usados son una funcionalidad muy visual y personalizable de **GitHub Readme Stats**. Esta tarjeta muestra los lenguajes más utilizados en tus repositorios de GitHub. **Importante**: Solo considera repositorios públicos y no forks, a menos que configures tu propia instancia del servicio.

### **Uso Básico**

Incluye este código en tu README y cambia el nombre de usuario:

```markdown
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay)](https://github.com/anuraghazra/github-readme-stats)
```

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay)](https://github.com/anuraghazra/github-readme-stats)

---

#### **Personalización**

1. **Exclusión de Repositorios**

   Para excluir repos específicos:

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&exclude_repo=repo1,repo2)](https://github.com/anuraghazra/github-readme-stats)
   ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&exclude_repo=repo1,repo2)](https://github.com/anuraghazra/github-readme-stats)

2. **Ocultar Lenguajes**

   Para ocultar ciertos lenguajes:

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&hide=lenguaje1,lenguaje2)](https://github.com/anuraghazra/github-readme-stats)
   ```

    [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&hide=html)](https://github.com/anuraghazra/github-readme-stats)

3. **Mostrar Más Lenguajes**

   Para ajustar la cantidad de lenguajes mostrados:

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&langs_count=8)](https://github.com/anuraghazra/github-readme-stats)
   ```

    [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&langs_count=8)](https://github.com/anuraghazra/github-readme-stats)

4. **Diseño Compacto**

   Cambia el diseño a uno más compacto:

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=compact)](https://github.com/anuraghazra/github-readme-stats)
   ```

    [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=compact)](https://github.com/anuraghazra/github-readme-stats)

5. **Ocultar Barras de Progreso**

   Oculta las barras de porcentaje:

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&hide_progress=true)](https://github.com/anuraghazra/github-readme-stats)
   ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&hide_progress=true)](https://github.com/anuraghazra/github-readme-stats)

---

#### **Diseños Alternativos**

1. **Gráfico de Donut**

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=donut)](https://github.com/anuraghazra/github-readme-stats)
   ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=donut)](https://github.com/anuraghazra/github-readme-stats)

2. **Gráfico de Donut Vertical**

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=donut-vertical)](https://github.com/anuraghazra/github-readme-stats)
   ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=donut-vertical)](https://github.com/anuraghazra/github-readme-stats)

3. **Gráfico de Pastel**

   ```markdown
   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=pie)](https://github.com/anuraghazra/github-readme-stats)
   ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&layout=pie)](https://github.com/anuraghazra/github-readme-stats)

---

#### **Ajustes Avanzados**

- **Algoritmo de cálculo**:  
  
  Puedes ajustar cómo se calculan los porcentajes usando `size_weight` y `count_weight`:

  ```markdown
  [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&size_weight=0.5&count_weight=0.5)](https://github.com/anuraghazra/github-readme-stats)
  ```

   [![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=josuesay&size_weight=0.5&count_weight=0.5)](https://github.com/anuraghazra/github-readme-stats)

---
