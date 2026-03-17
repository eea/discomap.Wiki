# Workflows & guidelines

This section contains links to guidelines and templates related to handling spatial data in EEA.

## EEA Publishing Guidelines

Map services play a pivotal role in supporting the mission and core values of the European Environment
Agency (EEA). These services serve a wide range of purposes, from internal use to the dissemination of
public information, covering EEA's key thematic areas. Given the dynamic nature of the information and
the evolving requirements associated with these services, it is imperative that we establish and adhere to
a standardized approach for requesting and maintaining them.
In this document, we explore the essential guidelines and practices for service publication utilizing
ArcGIS Pro in conjunction with ArcGIS Servers and Portal for ArcGIS.
By following these recommendations, we can ensure the highest standards of data quality, streamline
workflows, and maximize the benefits of our GIS initiatives. Let us embark on this journey of effective
service publication and make a lasting impact in the world of geospatial information.

**Projection**:  
  - The preferred projections for web mapping services are **WGS 1984 Web Mercator (Auxiliary Sphere)** or **ETRS89 / LAEA Europe (EPSG:3035)** for consistent geographic representation.  
  - Avoid mixing different projections within the same map service or product.  

**Layer Settings**:  
  - Symbology should be simple and consistent for clear map interpretation.  
  - **Scale-dependent rendering** is essential to optimize map performance.  
  - Ensure only necessary fields are visible; remove redundant ones.

**Geometry and Data Integrity**:  
  - Regularly check and repair geometries to avoid errors.  
  - Index key fields for performance and query optimization.  
  - Use **simple geometries**; multipart features should be avoided unless necessary.

**Metadata**:  
  - Complete metadata for all datasets and map services.  
  - Include important metadata like purpose, extent, data sources, and update frequency.  
  - Ensure metadata is compatible across all platforms (ArcGIS Server, Portal).

**Naming Conventions**:  
  - Follow standardized naming conventions to ensure consistency across services.  
  - Avoid special characters, spaces, or unnecessary abbreviations.

**Data Consistency**:  
  - Maintain consistency in field names and data types.  
  - Perform data validation and quality checks before publishing.

**Publishing Workflow**:  
  - Test map services in a **test environment** before deploying to production.  
  - Validate the functionality and performance of services to ensure they meet requirements.

> ➡️ **Full details**: **[Publishing guidelines](https://discomap.eea.europa.eu/doc/EEA_PublishingGuidelines.pdf)**

## EEA Design System

EEA's catalogue of everything that makes up your digital product including user interface elements, writing style, guiding principles, coding standards, visual design, etc. using reusable components for easy development. EEA Design System (EEA-DS) standardizes the visual language and user experience of the EEA’s online applications. This also allows us to be more effecient when creating online applications instead of reinventing the wheel over and over. EEA-DS was built by a multi-disciplinary team of developers, designers, UX researchers, writers and data scientists. Combining the expertise of all of these roles allowed us to create a design system with a wide range of elements and for various target users (Web Designer, Web Writer/Content manager, Web Developer and Data scientist).

> ➡️ **[EEA Design System](https://eea.github.io/volto-eea-design-system/)**