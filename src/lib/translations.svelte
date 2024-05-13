<script context="module" lang="ts">
  export interface Translations {
    [locale: string]: {
      [key: string]: string;
    };
  }

  const translations: Translations = {
    ru: {
      "main.logo.src": "images/logo/ru",
      "design.title": "Мы предоставим лучшие решения для вашего бизнеса",
      "design.strict": "Строгий",
      "design.delimiter": "или",
      "design.catchy": "броский",
      "bonuses.adapt.title": "Адаптируем ваш дизайн",
      "bonuses.adapt.image.src": "/images/placeholder-image.webp",
      "bonuses.adapt.image.alt": "Пример адаптации дизайна",
      "bonuses.delimiter": "или",
      "bonuses.create.title": "Создадим его с нуля",
      "bonuses.create.image.src": "/images/placeholder-image.webp",
      "bonuses.create.image.alt": "Пример создания дизайна",
      "whyus.title": "Почему именно мы?",
    },
  };

  export { translations };
</script>
