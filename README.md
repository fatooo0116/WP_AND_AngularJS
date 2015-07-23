# WP_AND_AngularJS
Integrate  Wordpress  And  AngularJS


# 1.OLD  XHR Ajax
                    var req = {
                        method: 'POST',
                        url: '/wp-admin/admin-ajax.php',
                        headers: {
                            'Content-Type':'application/json'
                        },
                        params: {
                            action: 'wdr_ajax_get'
                        }
                    }

                    $http(req).success(function(data){

                            $scope.firstName = data;

                            console.log(data);

                        }).error(function(){
                            console.log("error");
                        });

# 2. Speed UP AJAX

    // Force a short-init since we just need core WP, not the entire framework stack
     define( 'SHORTINIT', true );


