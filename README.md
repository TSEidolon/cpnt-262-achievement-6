# CPNT-262 Achievement 6 - Vue Components

 - v-slot was confusing. I understood the theory but in practice, I did not know what to do.
    - Apparently it imports a “child” component along with everything inside (template, script, styles) into a certain “space”
    - <a href="https://vuejs.org/guide/components/slots.html#slot-content-and-outlet" target="_blank">Vue tutorial on Vslots </a> helped immensely to put the v-slot theory into practice. 
    - Anything above or below `<slot/ >` will show in relation to their position.

```
    <ChildVSlot> 
      <!-- The <p> in ChildVSlot will output here -->
      Click Below  
    </ChildVSlot>
```

- `v-for` and `v-bind` went well due to the tutorial space in vuejs <a href="https://vuejs.org/tutorial/" target="_blank">VueJS tutorial </a>.

