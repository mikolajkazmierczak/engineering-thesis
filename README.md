# Engineering Thesis

## "Web system supporting product catalog management and client queries"

This project was created for [REED](https://reed.kalisz.pl/) company that specializes in comprehensive printing and advertising services.
They needed a web-based system designed to support product catalog management and handle customer inquiries. It consists of two main components: a public-facing website and an admin panel.

The system addresses the limitations of the client's existing solution, such as slow loading times, a cumbersome administrative interface, and the lack of personalized price calculators. The new system is tailored to the client's needs, with some key improvements:

- much more productive pricing panels,
- simpler menu, category and file management,
- less cluttered, more intuitive product display,
- streamlined inquiry form.

### The Public Website

The public website enables customers to browse products, view detailed information, and submit inquiries. A simple menu was provided that allows to gradually expand nested categories, thus filtering the products.

![publiczna_strona](screenshots/publiczna_strona.png)

![produkt](screenshots/produkt_1.png)

### The Admin Panel

The admin panel was built to manage calculators, products, colors, categories, menus, pages, customer inquiries, and some distinct website fragments. It includes features like hierarchical category and menu organization, handling images and files, but most importantly **automated price calculators**, which significantly improve workflow efficiency. Administrators can easily adjust pricing of multiple sets of products based on customizable calculators based on arbitrary parameters.

#### Content Management

The management of products, colors, categories, menus, pages and certain website fragments all happens in visually similiar panels. Products can be assigned to multiple categories and colors. You can also upload images and files.

![product list view](screenshots/widok_produkty.png)

![single product view](screenshots/widok_produkt_1.png)

<p align="right">
  <img src="screenshots/widok_produkt_4.jpg" alt="product pricing view" style="width: 80%;">
</p>

<p align="right">
  <img src="screenshots/widok_produkt_6.png" alt="product colors view" style="width: 80%;">
</p>

![alt text](screenshots/widok_kategorie.png)

![alt text](screenshots/widok_pliki.png)

#### Inquiries

A section of the panel is dedicated to managing customer inquiries, as well as adding inquiries not directly submitted through the website.

![alt text](screenshots/widok_zapytania.jpg)

#### Calculators

Without a doubt, the most important feature of the admin panel is the **automated price calculators**. They significantly reduce the time spent on manual calculations and ensures consistent pricing in all products.

![alt text](screenshots/widok_kalkulacje.jpg)

#### Development

The project was developed using agile methodology, with iterative feedback from the client ensuring the system met their expectations.

Technologically, the project leverages Directus (a Backend-as-a-Service solution) for database and API management, ensuring scalability and ease of maintenance. The frontend is built using SvelteKit, chosen for its performance and developer-friendly approach. WebSockets were also introduced (via a custom server aptly named "Heimdall") to enable real-time updates for the admin panel.

| Architecture Diagram                                                                | Use Case Diagram                                                                 |
| ----------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| <img src="screenshots/architektura.png" alt="architektura" style="width: 390px;" /> | <img src="screenshots/usecase.jpg" alt="usecase diagram" style="width: 420px;" > |

### Feedback and Results

Elementary usability tests confirmed the interface's intuitiveness, and performance benchmarks showed significant improvements over the old system. Adding a typical new product from scratch now takes 76 seconds compared to 442 seconds previously. Future enhancements will include automated price and inventory synchronization with external suppliers (via their APIs), scheduling tools for automatic product publication, and further UX improvements both in the admin panel and the public-facing website.

This project demonstrates my ability to deliver a comprehensive, real-world, customer-driven solution that combines technical expertise and a focus on user experience.
