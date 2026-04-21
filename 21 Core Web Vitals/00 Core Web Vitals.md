# 📊 Core Web Vitals – Complete Guide

## 📌 What are Core Web Vitals?

Core Web Vitals are a set of standardized performance metrics defined by Google to evaluate **real-world user experience** on a website.

They focus on three critical aspects:

* 🚀 **Loading performance**
* ⚡ **Interactivity**
* 🎯 **Visual stability**

These metrics are measured using real user data (field data) and are used across tools like:

* Chrome DevTools
* Lighthouse
* PageSpeed Insights
* Search Console

---

## 🧩 Core Web Vitals Metrics

### 1️⃣ Largest Contentful Paint (LCP)

![Image](https://images.openai.com/static-rsc-4/SLQzuaQIOSFcA8GToHQNLc2at_bkGyK-ZPu1jYvciGnUimX4Hma9h1Z5uOeSWY4mgX3X1DgweYOjoH0AsRTt78vaUWHkzpp9mH4txIlkH_QWUU45uo-WN1bDTZ_gabsgxEK9HzW7X78keIIdcQssMh1BXF0wl2DPD43p_XMByI0MWxcMhNKPsQsVwm_Gt8Nz?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tvKgigLFCR71gFgrLm7xGiSPfvbjPeAd8aApEYg-tZFchWbJ2A7qbqJT3nR3zSBjI491Ng7id0SDToKQbtYLScJkSpSpNBUSk1E8KY20qT_Oj9JFA1CUGJKVuB1TCiTF8bDJVZEzl42H2f4prjXY4CTeuWVv1pxveGb_IXbP7RdHSgfHBv0MKccW-t0Crbel?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/xiROrLfSxhMtw4DVUj4daAK4OC9ZCKNgglHtR8vGnIRZE7fvdpZelBBla9L-nTJzEYq8zpPUSxXgi5_EdTB_JSYClF1hw7Eugo4wNuY7fR1SA_rmv7pNCA6jfX59qrHQP-sSz8wIJFDAeKSrALaZ9p0BKjzWSh-n5PU76hqVFpGIazV3LpHXHn4ayWVeWjYE?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/NdGthGJjhkHgWdaWXhJsgbu0Adyr1TePSzm3o9JFkPCuNIeWQVcjD2Z8UXz2zUX-Ryp_ouvRN7W2I8qVb_KaY14Nq2DcQsfC4HLT5eG708CYioYcyUTj3BrzRYcmnNgFt2a77JlosZ46r128qVnOOmZoJ7A-Ufkqgi_aSoNT8nWXsfCxvaHQTXB-lk8t-jtZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/pGTQZRLfwN--pP60IyS24ZCk8r-Mjlj8Qnc3w0NHUBjyl0IOxhYLmx0rrMY2v4a_ZtWoxCFtTToM573aDfQEqqWSWsp8i721m5nJEXtu1aCbJamCHUtTCh1N7myDMeUX5yLZ4iPzRO8zO_fQ-FKabxuXPxmERz8zqot2Jzg9NPWMIOmfbO5PPKMHSUDfdd-1?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ZMn6eLWf_QiNIJpaEaBK6KGHyfCo_1IC-wqmhBYNXj_zvgU7JxRe2SfUupag3Qmv6jyEfVk8ju0qKtS_KezNVJPZR8uxu52qPNG6emOfknIkWBiY65jwyyN9YuL_xpykdvsYOwUAyDNsqH0dmdOzshnRiTcz0svu-0lyh575BYHN-zqQHpnV-_RaBck45jXT?purpose=fullsize)

**Definition:**
Measures how long it takes for the **largest visible content element** (image, text block, etc.) to render.

**Why it matters:**
Indicates how quickly the main content becomes visible.

**Thresholds:**

* 🟢 Good: ≤ **2.5 seconds**
* 🟡 Needs Improvement: 2.5 – 4.0 seconds
* 🔴 Poor: > 4.0 seconds

---

### 2️⃣ Interaction to Next Paint (INP)

![Image](https://images.openai.com/static-rsc-4/iIfudEWp9zp7RvsKDozZk_WnveuUzS5vhyHypJe8EIYHnTZg4A8IMOL31SoDp4KDtrrJGyIs7MI9NYvK_xpDQLMQO8lqZ3nXXzQuiKREbQXLQgAe5Q_m__FmLkYr20zq3CeOeoXlstjn9woWEECiEMBLH478ImRPhLIW1NXPKbF3CTq19kDufu2wbEOEJAxR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/dlg7M8myQwiLJr1epUZ5rBuiyjp6HHmBpTmoX8eZm5O3w6eOxEq1vHL-xn0tjrEwQPw6ZJvtB1PMNBaYQUN8m-BEMtjfKgmUpMFK5udElj0wrs8DQWO_Uybx_zHXwc0y8eRqTEaO4gO7r_6DuNnzIXVJGAJg118O2VhJ5wtCbPA_cKWhx5evrqbJkPD62J7J?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/5PKSsOrGeNDRy5T0i4RoOrkQE0Y5EFoonU6AbIkJMfK40Qg6uoD0bRj9zkP-yvHh99tv53y76Y-rWKJZ_wQK3AHxapkdRCYN-ffAqHJ1dbFVikRJ5NrFXytTAxryD5C1PaTrGHRqbNVoBEp2EWQMoWNFq_H89pVLdcpi3E_2JRraS8HBTZKbTW5yKk9IxiqL?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/zo4Vo7V8K6Ifo18co0zHFvPCx4oyioUfmQcf9Xi2d5qKEky3q28IQsoQ4z3ofFvAmf6_LuZAsaC7J7FQFokErzBUFxHT04Cyr3RgMPfTUrXuOaxpK9YRsp0ur9GtJP5yPqTIiZPDXoQsw4OIjOfC3laI-g20-ccUpODIs3WzVaM3JM0QBRSGPYuuIGt7oFVF?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/acjjzz8prW2q1YgGzC5zWizanuZIDPtCUC39U8d3UEiQu_mNLHSVkaFXxkD1wAvATVxi4WE_ZA3RHU0HvGIlqeTKfwvDe5jqDXjCVozG-2pUY8AnM8-uxcE2Ca8KZMOjh91XCRD3z5c1XsyrV-_2wXPBAzSfrnow1Jq-6Kz_nhgOuou4Jw2d2J_NntfHCMIp?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/lidl1YdYNkrlJObev0cb3F-K-3wkOLhzxfbUweiACaCr33uFzxSvMrc1gTjpKlKrFhXqphoH6Ssbo0OYOeiG-HXTy77wMnueIALRyAW30u4WUWYDAohHyACYztTQmobVT1aKumGhT57NNNFFcw5MjHFDm3R2zWnDti3DoRXkVr3O8NnPHwjiqXtJ8E1s9C5n?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/WLE6s3ve5sIQNJyhbquXK9Pbu2pTZDHz9hEUmAOEaxFm0LWXu1UML6gQ8_FsVlWM7jteNTn8cOy2acCMSKLRuLcyOBo5xFVirOay_CK_8MACBZtAdCq9-T4zWJ0FYg-9IJ76MKoTw2ZXXHdRKmO6UM356kL9opfUOIvLK_Hmfn2xeTeRVlpxjrS5XrQhz8yY?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/kX7bZpmXxwFJaAcm7t6h7WA-BriIF-vfzCep6d8qnj0K2F3s8vAD-BMgRAJLtLFzocEkkFh3w2Un56TStijOc5y8hQUrFhyS_t3wy4W2G_0xTDCaURzlrEa40CTzE5PNl8svPjIanSqaHVbmx-OUxjlKo_Ko83gypAWB_uhqqLJ166fqW5kkc8pu2wEJtajZ?purpose=fullsize)

**Definition:**
Measures responsiveness — how quickly the page reacts to user interactions (click, tap, keyboard).

**Why it matters:**
Represents **real interaction delay**, replacing older FID (First Input Delay).

**Thresholds:**

* 🟢 Good: ≤ **200 ms**
* 🟡 Needs Improvement: 200 – 500 ms
* 🔴 Poor: > 500 ms

---

### 3️⃣ Cumulative Layout Shift (CLS)

![Image](https://images.openai.com/static-rsc-4/CeK7qHqflc5tAwJPMvwKgzs1GMvufwxPtDNNaFzMe8HwnA0_FWzl-6Sr7jGcjNiblUVSQkyqxwZ6Jcoxenqw-zmuRjlIEqaTUV3JQjFHqDq0XCN3c0L0V9yMND0UVSXheqiZKBck9FDUN69MhXsOdObHOP5NeN8V63SUkcEIr1tuz4c4aJklQnmeHT5XisEg?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ashVX7i36n4mshJNEb4WGcLz2LprPlN7EgeXSic1lj5Ze8cI6t5vAWpX8ElPZTYofHingzBgSmoAztCPrP8P-fH4mgoxFELTSdiCGb9IJO0jXNcdqFkme4MdmR0smvDFehxvBMFTfVHgti7RRQPSLUQzDZI_1an4sgaEa_nre8FywcudETnlDdD5DI2h2E4r?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/5Z3BEwCzlYx8unwGxaNpoOukxG1ABERguJNhyCb4pGGhU4DQ0hz_wcJhosVH7GR-tOQ9_wmEHwQHKm_-VM3okdgqOfyg7dTZ3IXkF8IvELXUo2zVAjAtERcWAGrUVkFeiHVZKarMjniAMZzejXh1_78Jv1xIiUEracCCfnFTJJccyHHBcyBw1PoPEwebVqA5?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/T62XyAdr7vES5QiSTRAAg-C0tlMlyENyACUXMnGtKQxsg1l5F9pm1F7JRQ0tQUA634ginSNCCeP8Q-6ZUkCpy84Fq6F-dUUWdD1ZTiz_5OiclYT8FF9zkHfDGIIpxCNPFJN-dbS2hXKVPCiJlsD-d3lD2CA3boLcNSh1pv0GIHSIA_IJNUn3cvZHLxOhcsfw?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/A2FQHIy_vTX2vJvSE4qUDZElf2oZLSz_RhPPA6q-ib5QmlIThtCeY9GIEt8jpfzHmrJhITh97aIEsqUqGBqLdp9q6V151PnzjDLliIsSysXDS3qGwnA-wbG1N3MKWoAj1QyOwnHL6WLIoJkgYg_jp9QkCZQGWLXJkvV65pNAOVvC8KQlJTgZWOwFMraDd8Ch?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/yGYEtBjt8darxYK1x6Kyz6kBdf0k5aQcT5Nz3p7GfVHHBkeElLLS1uqBF18LGcm3lk2NRTcUEIXwkcF5lbByLTnmsGCTXYY7-DiboYuzEYisRwKKka8xroxx4Zt03xsjlLg8AQqB4QyhzuqvQyVXu7VhMcUIyFSYRw166OJFEJMH7CC2kaaZWaKkDwWvss77?purpose=fullsize)

**Definition:**
Measures unexpected layout shifts during page load.

**Why it matters:**
Prevents frustrating experiences like clicking the wrong button.

**Thresholds:**

* 🟢 Good: ≤ **0.1**
* 🟡 Needs Improvement: 0.1 – 0.25
* 🔴 Poor: > 0.25

---

## 📈 Measurement Strategy

* Use **75th percentile** of page loads (important detail from your image)
* Measure across:

  * 📱 Mobile
  * 💻 Desktop

👉 A page passes Core Web Vitals only if **all three metrics are within "Good" range**.

---

## 🧪 Performance Case Study: Lazy Loading Optimization

### 🔴 Before Optimization

![Image](https://images.openai.com/static-rsc-4/Q5IpmAKjl6Le_fqfFPX556vaRZmceQvMf8OBEbKe_to4BCBHrBIrtA9KeTyQXuojZ6byTiy0IM0V9eySOmK3ljJrLdSaxPCd9GuE-VVBJGEbt4mQJ8dXA0a2JIX7Xh4mjvHkcLoJcLiGGVOkwWQUThEtpKegC70UNZzKyT79MLjPAXcJcs65AwyVOrQXB7JM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/zZ9zxhophlreDResIIkNX3JnyDj7lEcUXeU-7z-SZwghyXVR6Dh4Grc-HvhzJhTKBD43JxZnu0GDjj5UFj3Fu6EubOSnhvYE7kxPfyvBXaI9JYEqGXazLG17i75JXqWAf7dHs2UuqH7F1dEHiZ2a9UYu6jqcL4SLO21rLXyUweokV3AjzzThTHb0m9nyvKED?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/nzc10TByIiILDWYSVqI2agaUbFFm9rV2EMymoWcogdNTb4gLU3OZbgM9RVOYFDc-YTsfP0gb1M8BT6BKxLYxFUvh1HzcXOyzvXwtCUyqSzHJoqGKqO_xDzX-3QYtsPG9XjXuoLRB0qO_odl9B8t4i4LBkXlKbLXN7e5PuCX-yI6buP5p0e0YeoNQA2N2_BZ9?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/A2FQHIy_vTX2vJvSE4qUDZElf2oZLSz_RhPPA6q-ib5QmlIThtCeY9GIEt8jpfzHmrJhITh97aIEsqUqGBqLdp9q6V151PnzjDLliIsSysXDS3qGwnA-wbG1N3MKWoAj1QyOwnHL6WLIoJkgYg_jp9QkCZQGWLXJkvV65pNAOVvC8KQlJTgZWOwFMraDd8Ch?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/t6fStd-8Juv5TRw9mzhzabLkoy1yjuRg7vCn0sAij_e9Bof1mPmPAhN4oi7rmjMeArc_l2Uvz1zfW3qLE2-v1lkggRGjJGM7v_xXsVercvVheZF1f_Ki4z9xgiDOzXTxE_M4g7bDiYvUuJY2v4NMisFTbBazjPKCsxnu8qHdpLTYahXVWuCLtGp6KJQs0R6G?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tAYPJ0l2aM8WjRqGJPsVKvipQ6dpCqZpkmNsb4URj19ldoOUYDqCo9N6M0ZzTj17j0CbRTbYOxW8rbzz4MNnxTF9KevnheGJiLXdg9uVYZb-iHd1z0qlcoWvYY3WV2Ev5Yc2-DN0rWOU9_4TBqyZZxKIHGkMp1afsY7bsjR62DXTyG6ikmgUUk6L8e5ayJhJ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/I8XFsgR48W2duKmD4juQXuqMYHJSwE0eIQDTR8jouh12RvW59PvmhoHnAs3RG5faD3lkUwg8HLwcFE-j2z2XCrX6tkcVE26kFdF7breK05ItaLX8E8oXF4rYr6-tWEeZLkwTRnFj0F1S90Rc84YnlLDd7dbzOEIiIxwkcbG1J9e1Qxcn8OeSCc6SNN2ky_OZ?purpose=fullsize)

**Scenario:**
No lazy loading applied to images.

**Observed Metrics:**

* First Contentful Paint (FCP): **~1.37 s**
* Largest Contentful Paint (LCP): **~2.00 s**

**Problem:**

* All images (including below-the-fold) load immediately
* Network congestion
* Slower rendering of important content

---

### 🟢 After Optimization (Lazy Loading Enabled)

![Image](https://images.openai.com/static-rsc-4/t6fStd-8Juv5TRw9mzhzabLkoy1yjuRg7vCn0sAij_e9Bof1mPmPAhN4oi7rmjMeArc_l2Uvz1zfW3qLE2-v1lkggRGjJGM7v_xXsVercvVheZF1f_Ki4z9xgiDOzXTxE_M4g7bDiYvUuJY2v4NMisFTbBazjPKCsxnu8qHdpLTYahXVWuCLtGp6KJQs0R6G?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ZpD_1DSMdz7wxdmHjtmT0O08uaxbUIh0oyd8Zc0D4OiY8AIhiXHDVTlnXoLr-ChBgIZypu-yHsl3KMgGba3Rxayn6Irt5hXTYWfB_EoKl9KLQAYBQNmGh4Dni9oyDqX-i5VTysz_8Pg7-c6fWiLLZ6q-0J_hvFlmLkkviDWoIgEfaBRRNEpZtIOxg35Wt9_w?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/zZ9zxhophlreDResIIkNX3JnyDj7lEcUXeU-7z-SZwghyXVR6Dh4Grc-HvhzJhTKBD43JxZnu0GDjj5UFj3Fu6EubOSnhvYE7kxPfyvBXaI9JYEqGXazLG17i75JXqWAf7dHs2UuqH7F1dEHiZ2a9UYu6jqcL4SLO21rLXyUweokV3AjzzThTHb0m9nyvKED?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/7g2F-_eg8TGazmavyvhYliUJp7_0YSjcx2mNL7aKyDhw-uTKJhlBmp-G3073s0Seui0KhjY66Q4K_IO_0zDheoJzP_6rQT5GZOwYNCoEm-nPFd0heU0hWDJ4WXeMJTnJ-CkMPvaRZgWtWNzOpxcNuQu9uj8IQdccgMWoNIPc2TDnwESY3VBE1AkFd-OdZFE2?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/g_DsIHGohpbaYc1ZDxEB8LKSt5svS8LR-TCMPwvKzobpzfHSwOiPU56Si_mcy2ebmnQdt4j0fo2xRSALIDG--bn-KvAvhmNWL-W_AM0uzN403wSYBA1R9zHeGk9pQFKikR29O79nxnjDkeMiL1P8eFkEUMfe9h-B-kfhx4mW2aoAnlFQr-RaoJIWoTgvPOa8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/87VIqr3MIXYktWhGbyG6aPG43UFGpINWP3S9wkqJ5Z7vf6WUUT5YgcnJefv7A-J8O9xHoLss8khbP8LZEBIJKClRS22EUzLuB0c7n4sDhiwlDqwIcTyAi1LaKNP9Z4K4Ahc1u09MNfo5qhMXAgsy1WIQ2jSul3FfKsNnuA2dI3nfw2la_9IBDBBTios9wIQu?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/197CQTktFt6DnVG7dj21KSDNYnuwtMtCcIqRNCQ4c-PBmdVqRk0GOJpuN_o-9n4S9ve1Nfz0BEMx6EVJDZUy8DcGOJAgqteHEkbZVc_o2iZ8AjvuU1fAOI9CRjG68tYetXSEKzv0llPNyflRt_uq7-JU2DY8xm4ScAoqzDRRZnmDbnWE6nLSN4t12SzkVIvd?purpose=fullsize)

**Scenario:**
Images below the fold are lazy loaded.

**Observed Metrics:**

* First Contentful Paint (FCP): **~608 ms**
* Largest Contentful Paint (LCP): **~1.18 s**

**Improvements:**

* Faster initial render
* Reduced resource blocking
* Prioritized above-the-fold content

---

## ⚙️ Key Optimization Techniques

### 🖼️ 1. Lazy Loading Images

```html
<img src="image.jpg" loading="lazy" alt="example" />
```

---

### 🚀 2. Optimize LCP

* Use modern image formats (WebP, AVIF)
* Preload critical assets:

```html
<link rel="preload" as="image" href="hero.jpg">
```

* Reduce server response time (TTFB)

---

### ⚡ 3. Improve INP

* Minimize JavaScript execution
* Use code splitting
* Avoid long main-thread blocking

---

### 🎯 4. Reduce CLS

* Always define width & height for images:

```html
<img src="image.jpg" width="400" height="300" />
```

* Avoid dynamic content shifts
* Use reserved layout space

---

## 🧠 Important Insights

* Core Web Vitals are **user-centric**, not just technical metrics
* Performance directly impacts:

  * SEO rankings
  * Conversion rates
  * User retention
* Even small optimizations (like lazy loading) can drastically improve scores

---

## 🏁 Summary

| Metric | Focus            | Good Threshold |
| ------ | ---------------- | -------------- |
| LCP    | Loading          | ≤ 2.5s         |
| INP    | Interactivity    | ≤ 200ms        |
| CLS    | Visual Stability | ≤ 0.1          |

---

## 📚 Final Takeaway

If your site:

* Loads fast (LCP ✅)
* Responds instantly (INP ✅)
* Doesn’t shift unexpectedly (CLS ✅)

👉 You deliver an **excellent user experience** and align with modern web performance standards.
