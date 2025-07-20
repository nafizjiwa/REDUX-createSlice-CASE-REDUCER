# REDUX-CREATE-CASE-REDUCER

- Create a reducer using a slice

        --SliceFile.js--
        import { createSlice } from '@reduxjs/toolkit';

    const sliceName = createSlice({
        - Slice includes
            name: 'SliceName', 
            initialState: Slice's InitialState,
            reducers: {                         //Define how to handle and process the action payloads
              caseReducer1: (state, action) => {
                    console.log(action.payload)
                    },
              caseReducer2: (state, action) => {}
               } 
     })

     expport const { caseReducer1, caseReducer2 } = todoSlice.action;
     export default sliceName.reducer;


  - To use the slice in the App Component use the useSelector();

    import { useSelector, useDispatch } from 'react-redux';      //import useSelector and useDispatch
    import { caseReducer1, caseReducer2 } from './sliceFile';              //import action reducers from slice
     
    const App () => {
            const sliceName = useSelector((state)=> state.todos)      //useSlector help retrieve the state needed
            const dispatch = useDispatch();                           //use dispatch to access the reducer defined in theslicefile
          if(){
            dispatch(caseReducer1)                                         //then use dispatch to dispatch the reducers action
          }
      }
  
  
