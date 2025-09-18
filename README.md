# REDUX-createSlice-CASE-REDUCER

### - Create a reducer using a slice

        --SliceFile.js--
        import { createSlice } from '@reduxjs/toolkit';    //In the sliceFile import createSlice

        const sliceName = createSlice({                          - Slice includes
                 name: 'SliceName', 
                 initialState: Slice's InitialState,
                 reducers: {                        //Object of functions
                         //Reducer defines how to handle and process the action payloads
                   caseReducer1: (state, action) => {
                        console.log(action.payload)
                        },
                   caseReducer2: (state, action) => {}
                        },
         })

         expport const { caseReducer1, caseReducer2 } = todoSlice.action;  //export the case reducers
         export default sliceName.reducer;                                 //export the sliceReducer


### - To use the slice and its reducers in the App Component use the useSelector() and useDispatch;

        import { useSelector, useDispatch } from 'react-redux';           //import useSelector and useDispatch
        import { caseReducer1, caseReducer2 } from './sliceFile';         //import action reducers from slice
     
        const App () => {
                const sliceName = useSelector((state)=> state.todos)     //useSelector help retrieve the state needed
                const dispatch = useDispatch();                    //use dispatch to access the reducer from the slicefile
                if(){
                  dispatch(caseReducer1)                                 //then use dispatch to dispatch the reducers action
                }
        }
  
  
