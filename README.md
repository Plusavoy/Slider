# Slider


let slideIndex = 1, //Слайд который будет виден по умолчанию

        slides = document.querySelectorAll('.slider-item'), //Отдельный слайд
        
        prev = document.querySelector('.prev'), //Кнопка назад
        
        next = document.querySelector('.next'), //Копка вперед
        
        dotsWrap = document.querySelector('.slider-dots'), //Блок с точками
        
        dots = document.querySelectorAll('.dot'); //Каждая отдельная точка
        
        #Dots //Если не нужны точки - удаляем эти строки кода и переменные dotsWrap и dots.
        
        dotsWrap.addEventListener('click', function(event) {
        
            for (let i = 0; i < dots.length + 1; i++) {
            
                if (event.target.classList.contains('dot') && event.target == dots[i-1]) {
                
                    currentSlide(i);
                    
                }
                
            }
            
        });
        
