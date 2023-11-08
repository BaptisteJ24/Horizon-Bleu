<template>
  <nav className="nav">
    <button className="nav__btn">
      <span className="fa-solid fa-bars fa-lg icon-fa">
        <span className="sr-only">Ouvrir le menu de navigation</span>
      </span>
    </button>
    <div className="nav__bar" data-isopen="{isOpen}">
      <button className="nav__btn nav__btn--close">
        <span className="fa-solid fa-xmark fa-lg icon-fa">
          <span className="sr-only">Fermer le menu de navigation</span>
        </span>
      </button>
      <div className="container nav__list__container">
        <ul className="nav__list">
          <li className="nav__list__item" key="{index}"></li>
        </ul>
      </div>
    </div>
  </nav>
</template>
