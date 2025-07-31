<template>
    <div id="app">                                                           <!-- Root element of the app -->

        <!-- Main navigation bar using Semantic UI classes -->
        <div class="ui inverted segment navbar">                             <!-- Inverted color navbar using Semantic UI -->
            <div class="ui center aligned container">                        <!-- Center-aligned container for the menu -->
                <div class="ui large secondary inverted pointing menu compact"> <!-- Compact, large, inverted menu with pointing style -->

                    <!-- Router link for "Words" -->
                    <router-link to="/words" exact class="item">            <!-- Link to "/words" page -->
                        <i class="router outline icon"></i> Words           <!-- Icon and label -->
                    </router-link>

                    <!-- Router link for "New" -->
                    <router-link to="/words/new" class="item">              <!-- Link to create a new word -->
                        <i class="plus circle icon"></i> New                <!-- Icon and label -->
                    </router-link>

                    <!-- Router link for "Test" -->
                    <router-link to="/test" class="item">                   <!-- Link to test feature -->
                        <i class="graduation cap icon"></i> Test            <!-- Icon and label -->
                    </router-link>
                </div>
            </div>
        </div>

        <!-- Main content container for views -->
        <div class="ui text container">                                      <!-- Text container using Semantic UI -->

            <flash-message class="myFlash"></flash-message>                 <!-- Flash message component for showing notifications -->

            <div class="ui one column grid">                                 <!-- Grid with one column -->
                <div class="column">
                    <!-- Router view where components will be rendered based on the route -->
                    <router-view></router-view>                             <!-- This is where page components will appear -->
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'app' // Name of the component
};
</script>
<style>
#app .navbar {
    margin-bottom: 1.5em;                      /* Add space below the navbar */
}

.myFlash {
    position: absolute;                        /* Position the flash message box */
    top: 0;
    right: 0;
    width: 300px;                              /* Set fixed width for flash message */
}

div.label {
    width: 120px;                              /* Set fixed width for label blocks */
}

div.input {
    margin-bottom: 10px;                       /* Add spacing between inputs */
}

button.ui.button {
    margin-top: 15px;                          /* Space above the submit button */
    display: block;                            /* Make button take full width of container */
}
</style>