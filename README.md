# LMN_toolbox 1.5.1 with bug resolutions

1.  Original code assumes that input variables and the premise variables are the same. I have modified method
    calculateModelOutput to account for the premise variables being a subset of the inputs. However, property
    relationZtoX must be set appropriately prior to evaluating the model. Example usage code follows:
    
    LMN.relationZtoX = [ 4 5 ];             % only inputs 4 and 5 are premise variables.
    Yp = LMN.calculateModelOutput( X, Y );  % Evaluate the model.
 
